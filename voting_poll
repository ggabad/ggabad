import streamlit as st

st.set_page_config(page_title="Quick Voting Poll")
st.title("Quick Voting Pool")

question = "El EOY Toast será el mismo día de nuestra posada. Por lo que: ?"
options = ["a.Se queda como esta","b. Lo cambiamos de fecha al jueves 18","c.Cancelarlo por motivo de que mover la fecha a estas alturas ya puede ser complicado"]

st.write(f"### {question}")
choice = st.radio("Choose one option: ", options)

if "votes" not in st.session_state:
    st.session_state.votes = {opt: 0 for opt in options}

if st.button("Submit Vote"):
    st.session_state.votes[choice] += 1
    st.success("Your vote has been recorded!")

st.write("---")
st.subheader("Live Results")

for opt, val in st.session_state.votes.items():
    st.write(f"**{opt}** - {val} votes")
