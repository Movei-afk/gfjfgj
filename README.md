struct BottomTabBar: View {
    @Binding var showAddMeal: Bool

    var body: some View {
        HStack {
            Spacer()
            Button(action: {}) {
                Image(systemName: "house")
            }

            Spacer()
            Button(action: {}) {
                Image(systemName: "waveform.path.ecg")
            }

            Spacer()

            Button(action: {
                showAddMeal = true
            }) {
                ZStack {
                    Circle()
                        .fill(Color.orange)
                        .frame(width: 50, height: 50)
                        .shadow(radius: 4)
                    Image(systemName: "plus")
                        .foregroundColor(.white)
                        .font(.title2)
                }
            }
            .offset(y: -20)

            Spacer()
            Button(action: {}) {
                Image(systemName: "heart")
            }

            Spacer()
            Button(action: {}) {
                Image(systemName: "person")
            }
            Spacer()
        }
        .padding(.top)
        .background(Color.blue.opacity(0.9))
        .foregroundColor(.white)
    }
}
