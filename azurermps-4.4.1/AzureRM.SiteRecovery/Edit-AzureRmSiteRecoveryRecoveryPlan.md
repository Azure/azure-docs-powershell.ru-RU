---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 59C3E7D7-530F-4D07-904E-41610ECE9253
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Edit-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d5b7965ed6dea106a40a6be07171e9a3c258f5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732403"
---
# <span data-ttu-id="8bc07-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8bc07-101">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="8bc07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bc07-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc07-103">Изменение плана восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="8bc07-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bc07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bc07-104">SYNTAX</span></span>

### <span data-ttu-id="8bc07-105">AppendGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bc07-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bc07-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="8bc07-106">RemoveGroup</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bc07-107">AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="8bc07-107">AddProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bc07-108">RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="8bc07-108">RemoveProtectedEntities</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedEntities <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc07-109">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8bc07-109">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc07-110">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8bc07-110">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItems <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8bc07-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bc07-111">DESCRIPTION</span></span>
<span data-ttu-id="8bc07-112">Командлет **Edit-AzureRmSiteRecoveryRecoveryPlan** редактирует план восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc07-112">The **Edit-AzureRmSiteRecoveryRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="8bc07-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bc07-113">EXAMPLES</span></span>

## <span data-ttu-id="8bc07-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bc07-114">PARAMETERS</span></span>

### <span data-ttu-id="8bc07-115">-AddProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="8bc07-115">-AddProtectedEntities</span></span>
<span data-ttu-id="8bc07-116">Указывает массив защищаемых сущностей, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="8bc07-116">Specifies an array of protected entities to add.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: AddProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-117">-AddProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8bc07-117">-AddProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-118">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="8bc07-118">-AppendGroup</span></span>
<span data-ttu-id="8bc07-119">Указывает на то, что эта операция добавляет группу в объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="8bc07-119">Indicates that this operation appends the group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-120">-Группа</span><span class="sxs-lookup"><span data-stu-id="8bc07-120">-Group</span></span>
<span data-ttu-id="8bc07-121">Указывает группу планов восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="8bc07-121">Specifies a Site Recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddProtectedEntities, RemoveProtectedEntities, AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8bc07-122">-RecoveryPlan</span></span>
<span data-ttu-id="8bc07-123">Указывает план восстановления.</span><span class="sxs-lookup"><span data-stu-id="8bc07-123">Specifies a recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="8bc07-124">-RemoveGroup</span></span>
<span data-ttu-id="8bc07-125">Удаляет указанную группу планов восстановления для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="8bc07-125">Removes the specified Site Recovery recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-126">-RemoveProtectedEntities</span><span class="sxs-lookup"><span data-stu-id="8bc07-126">-RemoveProtectedEntities</span></span>
<span data-ttu-id="8bc07-127">Указывает массив защищенных сущностей.</span><span class="sxs-lookup"><span data-stu-id="8bc07-127">Specifies an array of protected entities.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: RemoveProtectedEntities
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-128">-RemoveProtectedItems</span><span class="sxs-lookup"><span data-stu-id="8bc07-128">-RemoveProtectedItems</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc07-129">-DefaultProfile</span></span>
<span data-ttu-id="8bc07-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc07-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc07-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc07-131">CommonParameters</span></span>
<span data-ttu-id="8bc07-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bc07-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc07-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc07-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc07-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bc07-134">INPUTS</span></span>

### <span data-ttu-id="8bc07-135">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8bc07-135">ASRRecoveryPlan</span></span>
<span data-ttu-id="8bc07-136">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8bc07-136">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="8bc07-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bc07-137">OUTPUTS</span></span>

## <span data-ttu-id="8bc07-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bc07-138">NOTES</span></span>

## <span data-ttu-id="8bc07-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bc07-139">RELATED LINKS</span></span>

[<span data-ttu-id="8bc07-140">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8bc07-140">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="8bc07-141">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8bc07-141">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)
