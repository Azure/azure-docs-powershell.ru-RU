---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076410"
---
# <span data-ttu-id="98c74-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="98c74-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="98c74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98c74-102">SYNOPSIS</span></span>
<span data-ttu-id="98c74-103">Запускает задание относительной связи в политике репликации, связанной с контейнером защиты для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="98c74-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="98c74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98c74-104">SYNTAX</span></span>

### <span data-ttu-id="98c74-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98c74-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="98c74-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="98c74-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="98c74-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c74-107">DESCRIPTION</span></span>
<span data-ttu-id="98c74-108">Командлет **Start-AzureSiteRecoveryProtectionProfileDissociationJob** инициирует задание на отсвязь в политике репликации, связанной с контейнером защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="98c74-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="98c74-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98c74-109">EXAMPLES</span></span>

### <span data-ttu-id="98c74-110">Пример 1: отмена связи профиля защиты</span><span class="sxs-lookup"><span data-stu-id="98c74-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="98c74-111">Первая команда получает контейнер защиты с помощью командлета **Get-AzureSiteRecoveryProtectionContainer** , а затем сохраняет этот контейнер в переменной $ProtectionContainer 01.</span><span class="sxs-lookup"><span data-stu-id="98c74-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="98c74-112">Вторая команда получает контейнер защиты и сохраняет ее в переменной $ProtectionContainer 02.</span><span class="sxs-lookup"><span data-stu-id="98c74-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="98c74-113">Последняя команда не отменяет профиль защиты от контейнера, хранящегося в $ProtectionContainer 01 в качестве основного контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="98c74-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="98c74-114">Команда не применяет контейнер, хранящийся в $ProtectionContainer 02, в качестве контейнера защиты восстановления.</span><span class="sxs-lookup"><span data-stu-id="98c74-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="98c74-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98c74-115">PARAMETERS</span></span>

### <span data-ttu-id="98c74-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="98c74-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="98c74-117">Задает основной контейнер защиты.</span><span class="sxs-lookup"><span data-stu-id="98c74-117">Specifies a primary protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c74-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="98c74-118">-Profile</span></span>
<span data-ttu-id="98c74-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="98c74-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98c74-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="98c74-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98c74-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="98c74-121">-ProtectionProfile</span></span>
<span data-ttu-id="98c74-122">Задает параметры профиля защиты для связи с контейнерами защиты.</span><span class="sxs-lookup"><span data-stu-id="98c74-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="98c74-123">Задает параметры профиля защиты, применяемые к контейнерам защиты.</span><span class="sxs-lookup"><span data-stu-id="98c74-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="98c74-124">Чтобы получить объект **ASRProtectionProfile** , используйте командлет New-AzureSiteRecoveryProtectionProfileObject.</span><span class="sxs-lookup"><span data-stu-id="98c74-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98c74-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="98c74-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="98c74-126">Указывает контейнер защиты восстановления.</span><span class="sxs-lookup"><span data-stu-id="98c74-126">Specifies a recovery protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c74-127">CommonParameters</span></span>
<span data-ttu-id="98c74-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98c74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c74-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c74-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c74-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98c74-130">INPUTS</span></span>

## <span data-ttu-id="98c74-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c74-131">OUTPUTS</span></span>

## <span data-ttu-id="98c74-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="98c74-132">NOTES</span></span>

## <span data-ttu-id="98c74-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98c74-133">RELATED LINKS</span></span>

[<span data-ttu-id="98c74-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="98c74-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="98c74-135">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="98c74-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="98c74-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="98c74-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


