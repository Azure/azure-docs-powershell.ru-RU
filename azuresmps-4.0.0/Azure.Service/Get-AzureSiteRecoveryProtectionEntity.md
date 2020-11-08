---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075588"
---
# <span data-ttu-id="e9ca3-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e9ca3-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="e9ca3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ca3-103">Получает защищаемые или защищенные объекты в хранилище сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="e9ca3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9ca3-104">SYNTAX</span></span>

### <span data-ttu-id="e9ca3-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9ca3-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9ca3-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="e9ca3-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9ca3-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="e9ca3-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9ca3-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e9ca3-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9ca3-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="e9ca3-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9ca3-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="e9ca3-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9ca3-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9ca3-111">DESCRIPTION</span></span>
<span data-ttu-id="e9ca3-112">Командлет **Get-AzureSiteRecoveryProtectionEntity** получает защищаемые или защищенные объекты, например виртуальные машины, в текущем хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e9ca3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9ca3-113">EXAMPLES</span></span>

### <span data-ttu-id="e9ca3-114">Пример 1: отображение защищенной виртуальной машины в контейнере</span><span class="sxs-lookup"><span data-stu-id="e9ca3-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="e9ca3-115">Первая команда получает защищенный контейнер с помощью командлета **Get-AzureSiteRecoveryProtectionContainer** , а затем сохраняет этот объект в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="e9ca3-116">Вторая команда получает защищенную виртуальную машину, которая входит в контейнер в $Container, и выводит ее на экран.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="e9ca3-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9ca3-117">PARAMETERS</span></span>

### <span data-ttu-id="e9ca3-118">-ID</span><span class="sxs-lookup"><span data-stu-id="e9ca3-118">-Id</span></span>
<span data-ttu-id="e9ca3-119">Указывает идентификатор получаемой сущности защиты.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-119">Specifies the ID of a protection entity to get.</span></span>

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

### <span data-ttu-id="e9ca3-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9ca3-120">-Name</span></span>
<span data-ttu-id="e9ca3-121">Указывает имя получаемой сущности защиты.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-121">Specifies the name of a protection entity to get.</span></span>

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

### <span data-ttu-id="e9ca3-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="e9ca3-122">-Profile</span></span>
<span data-ttu-id="e9ca3-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9ca3-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9ca3-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e9ca3-125">-ProtectionContainer</span></span>
<span data-ttu-id="e9ca3-126">Указывает контейнер защиты.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-126">Specifies a protection container.</span></span>

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

### <span data-ttu-id="e9ca3-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="e9ca3-127">-ProtectionContainerId</span></span>
<span data-ttu-id="e9ca3-128">Указывает идентификатор защищенного контейнера.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-128">Specifies the ID of a protected container.</span></span>

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

### <span data-ttu-id="e9ca3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ca3-129">CommonParameters</span></span>
<span data-ttu-id="e9ca3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9ca3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ca3-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9ca3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ca3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9ca3-132">INPUTS</span></span>

## <span data-ttu-id="e9ca3-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9ca3-133">OUTPUTS</span></span>

## <span data-ttu-id="e9ca3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9ca3-134">NOTES</span></span>

## <span data-ttu-id="e9ca3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9ca3-135">RELATED LINKS</span></span>

[<span data-ttu-id="e9ca3-136">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e9ca3-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="e9ca3-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e9ca3-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="e9ca3-138">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e9ca3-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


