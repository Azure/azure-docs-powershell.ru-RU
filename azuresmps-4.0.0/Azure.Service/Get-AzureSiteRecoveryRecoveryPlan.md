---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075585"
---
# <span data-ttu-id="07d3c-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d3c-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="07d3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="07d3c-103">Возвращает план восстановления для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="07d3c-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="07d3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07d3c-104">SYNTAX</span></span>

### <span data-ttu-id="07d3c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07d3c-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="07d3c-106">ById</span><span class="sxs-lookup"><span data-stu-id="07d3c-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="07d3c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="07d3c-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="07d3c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07d3c-108">DESCRIPTION</span></span>
<span data-ttu-id="07d3c-109">Командлет **Get-AzureSiteRecoveryRecoveryPlan** получает план восстановления в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="07d3c-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="07d3c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07d3c-110">EXAMPLES</span></span>

### <span data-ttu-id="07d3c-111">Пример 1: получение плана восстановления</span><span class="sxs-lookup"><span data-stu-id="07d3c-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="07d3c-112">Эта команда получает сведения о плане восстановления для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="07d3c-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="07d3c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07d3c-113">PARAMETERS</span></span>

### <span data-ttu-id="07d3c-114">-ID</span><span class="sxs-lookup"><span data-stu-id="07d3c-114">-Id</span></span>
<span data-ttu-id="07d3c-115">Указывает идентификатор плана восстановления, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="07d3c-115">Specifies the ID of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3c-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07d3c-116">-Name</span></span>
<span data-ttu-id="07d3c-117">Указывает имя плана восстановления, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="07d3c-117">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d3c-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="07d3c-118">-Profile</span></span>
<span data-ttu-id="07d3c-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="07d3c-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="07d3c-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07d3c-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="07d3c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d3c-121">CommonParameters</span></span>
<span data-ttu-id="07d3c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07d3c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d3c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d3c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d3c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07d3c-124">INPUTS</span></span>

## <span data-ttu-id="07d3c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07d3c-125">OUTPUTS</span></span>

## <span data-ttu-id="07d3c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="07d3c-126">NOTES</span></span>

## <span data-ttu-id="07d3c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07d3c-127">RELATED LINKS</span></span>

[<span data-ttu-id="07d3c-128">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d3c-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="07d3c-129">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d3c-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="07d3c-130">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07d3c-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


