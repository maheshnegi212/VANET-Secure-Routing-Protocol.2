# VANET-Secure-Routing-Protocol.2
# VANET Secure Routing Protocol - Complete Project Documentation

## Table of Contents
1. [Project Overview](#project-overview)
2. [System Architecture](#system-architecture)
3. [Implementation Details](#implementation-details)
4. [Security Features](#security-features)
5. [Performance Analysis](#performance-analysis)
6. [Usage Instructions](#usage-instructions)
7. [Results and Findings](#results-and-findings)
8. [Future Enhancements](#future-enhancements)

## Project Overview

### Objective
Design and implement a lightweight, efficient secure routing protocol for Vehicular Ad Hoc Networks (VANET) that ensures data integrity, authentication, and protection against common attacks including impersonation, message modification, and replay attacks.

### Key Features
- **Multi-layered Security**: Digital signatures, cryptographic hashing, and salt-based protection
- **Real-time Attack Detection**: Automated detection of replay attacks, position spoofing, and message tampering
- **Realistic Vehicle Simulation**: Dynamic movement patterns with collision detection
- **Performance Monitoring**: Comprehensive metrics collection and analysis
- **Visual Analytics**: Multiple visualization tools for data analysis

### Technologies Used
- **Python 3.8+**: Core simulation engine
- **Cryptography Library**: RSA signatures and advanced cryptographic operations
- **Matplotlib**: Data visualization and plotting
- **Pandas**: Data manipulation and analysis
- **NumPy**: Mathematical computations and array operations
- **Hashlib**: Multiple hash function implementations

## System Architecture

### Core Components

#### 1. CryptographicManager
```python
Features:
- Multiple hash functions (SHA256, MD5, SHA1, Blake2b, SHA3_256)
- Salted hashing for enhanced security
- Performance monitoring and benchmarking
- Message integrity validation
```

#### 2. DigitalSignatureManager
```python
Features:
- RSA-2048 key pair generation
- PSS padding for enhanced security
- Message signing and verification
- Authentication mechanism
```

#### 3. Vehicle Class
```python
Features:
- Dynamic position and speed simulation
- Secure message creation and validation
- Trust score management
- Movement history tracking
```

#### 4. AttackDetector
```python
Features:
- Replay attack detection using message caching
- Position spoofing detection via movement analysis
- Message modification detection through hash comparison
- Suspicious activity logging
```

#### 5. CollisionDetector
```python
Features:
- Real-time proximity monitoring
- Collision risk assessment
- Distance-based alerts
- Safety metric collection
```

#### 6. VANETSimulator
```python
Features:
- Multi-vehicle coordination
- Message broadcasting simulation
- Attack scenario testing
- Performance metrics collection
```

#### 7. VANETVisualizer
```python
Features:
- Vehicle position plotting
- Hash performance analysis
- Security metrics visualization
- Real-time data representation
```

## Implementation Details

### Security Protocol Flow

1. **Message Creation**:
   ```
   Vehicle → Generate Message → Add Salt → Compute Hash → Sign Message → Broadcast
   ```

2. **Message Reception**:
