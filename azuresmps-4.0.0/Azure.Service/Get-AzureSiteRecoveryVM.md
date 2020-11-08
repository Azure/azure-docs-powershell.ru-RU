---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076569"
---
# <span data-ttu-id="45636-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="45636-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="45636-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45636-102">SYNOPSIS</span></span>
<span data-ttu-id="45636-103">Получение сведений о виртуальных машинах, управляемых с восстановлением сайта.</span><span class="sxs-lookup"><span data-stu-id="45636-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="45636-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45636-104">SYNTAX</span></span>

### <span data-ttu-id="45636-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45636-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="45636-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="45636-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="45636-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="45636-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="45636-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="45636-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="45636-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="45636-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="45636-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="45636-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="45636-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45636-111">DESCRIPTION</span></span>
<span data-ttu-id="45636-112">Командлет **Get-AzureSiteRecoveryVM** получает сведения о виртуальных машинах, управляемых в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="45636-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="45636-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45636-113">EXAMPLES</span></span>

### <span data-ttu-id="45636-114">Пример 1: получение сведений о виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="45636-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="45636-115">Первая команда использует командлет **Get-AzureSiteRecoveryProtectionContainer** для получения защищенного контейнера и сохраняет его в переменной $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="45636-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="45636-116">Вторая команда получает сведения о виртуальных машинах в $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="45636-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="45636-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45636-117">PARAMETERS</span></span>

### <span data-ttu-id="45636-118">-ID</span><span class="sxs-lookup"><span data-stu-id="45636-118">-Id</span></span>
<span data-ttu-id="45636-119">Указывает ИД виртуальной машины, о которой требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="45636-119">Specifies the ID of the virtual machine about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45636-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45636-120">-Name</span></span>
<span data-ttu-id="45636-121">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="45636-121">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45636-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="45636-122">-Profile</span></span>
<span data-ttu-id="45636-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="45636-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="45636-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="45636-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45636-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="45636-125">-ProtectionContainer</span></span>
<span data-ttu-id="45636-126">Указывает объект контейнера защиты для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="45636-126">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45636-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="45636-127">-ProtectionContainerId</span></span>
<span data-ttu-id="45636-128">Указывает идентификатор защищенного контейнера, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="45636-128">Specifies the ID of a protected container about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45636-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45636-129">CommonParameters</span></span>
<span data-ttu-id="45636-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45636-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45636-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45636-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45636-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45636-132">INPUTS</span></span>

## <span data-ttu-id="45636-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45636-133">OUTPUTS</span></span>

## <span data-ttu-id="45636-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="45636-134">NOTES</span></span>

## <span data-ttu-id="45636-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45636-135">RELATED LINKS</span></span>

[<span data-ttu-id="45636-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="45636-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


