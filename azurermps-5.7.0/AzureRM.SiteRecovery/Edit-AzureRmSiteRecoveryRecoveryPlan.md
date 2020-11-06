---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/edit-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8c078c97a1531863979b6182867e8900550b68b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567395"
---
# <span data-ttu-id="42bcb-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42bcb-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="42bcb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="42bcb-103">Изменение плана восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="42bcb-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42bcb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42bcb-104">SYNTAX</span></span>

### <span data-ttu-id="42bcb-105">AppendGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42bcb-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42bcb-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="42bcb-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42bcb-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="42bcb-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42bcb-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="42bcb-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42bcb-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="42bcb-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42bcb-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="42bcb-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42bcb-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42bcb-111">DESCRIPTION</span></span>
<span data-ttu-id="42bcb-112">Командлет **Edit-AzureRmSiteRecoveryRecoveryPlan** редактирует план восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="42bcb-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="42bcb-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42bcb-113">EXAMPLES</span></span>

## <span data-ttu-id="42bcb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42bcb-114">PARAMETERS</span></span>

### <span data-ttu-id="42bcb-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="42bcb-115">-AddProtectedEntities</span></span>
<span data-ttu-id="42bcb-116">Указывает массив защищаемых сущностей, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="42bcb-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="42bcb-117">-AddProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="42bcb-118">-AppendGroup</span></span>
<span data-ttu-id="42bcb-119">Указывает на то, что эта операция добавляет группу в объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="42bcb-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42bcb-120">-DefaultProfile</span></span>
<span data-ttu-id="42bcb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42bcb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-122">-Группа</span><span class="sxs-lookup"><span data-stu-id="42bcb-122">-Group</span></span>
<span data-ttu-id="42bcb-123">Указывает группу планов восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="42bcb-123">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42bcb-124">-RecoveryPlan</span></span>
<span data-ttu-id="42bcb-125">Указывает план восстановления.</span><span class="sxs-lookup"><span data-stu-id="42bcb-125">Specifies a recovery plan.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="42bcb-126">-RemoveGroup</span></span>
<span data-ttu-id="42bcb-127">Удаляет указанную группу планов восстановления для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="42bcb-127">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-128">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="42bcb-128">-RemoveProtectedEntities</span></span>
<span data-ttu-id="42bcb-129">Указывает массив защищенных сущностей.</span><span class="sxs-lookup"><span data-stu-id="42bcb-129">Specifies an array of protected entities.</span></span>

```yaml
Type: ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-130">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="42bcb-130">-RemoveProtectedItems</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42bcb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42bcb-131">CommonParameters</span></span>
<span data-ttu-id="42bcb-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42bcb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42bcb-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42bcb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42bcb-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42bcb-134">INPUTS</span></span>

### <span data-ttu-id="42bcb-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42bcb-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="42bcb-136">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="42bcb-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="42bcb-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42bcb-137">OUTPUTS</span></span>

## <span data-ttu-id="42bcb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="42bcb-138">NOTES</span></span>

## <span data-ttu-id="42bcb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42bcb-139">RELATED LINKS</span></span>

[<span data-ttu-id="42bcb-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42bcb-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="42bcb-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="42bcb-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
