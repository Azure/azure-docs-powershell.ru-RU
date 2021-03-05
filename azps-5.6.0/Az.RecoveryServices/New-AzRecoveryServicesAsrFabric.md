---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: bfea43fb0f27aff6405159c0174a698d9dc2298e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003139"
---
# <span data-ttu-id="05a52-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="05a52-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="05a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05a52-102">SYNOPSIS</span></span>
<span data-ttu-id="05a52-103">Создает ткань для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="05a52-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="05a52-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05a52-104">SYNTAX</span></span>

### <span data-ttu-id="05a52-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05a52-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05a52-106">Azure</span><span class="sxs-lookup"><span data-stu-id="05a52-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a52-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05a52-107">DESCRIPTION</span></span>
<span data-ttu-id="05a52-108">Для восстановления сайтов Azure указанного типа создается проектлет **New-AzRecoveryServicesAsrFabric.**</span><span class="sxs-lookup"><span data-stu-id="05a52-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="05a52-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05a52-109">EXAMPLES</span></span>

### <span data-ttu-id="05a52-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05a52-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="05a52-111">Начало создания ткань с переданным именем и возврат задания asR, используемой для отслеживания операции создания.</span><span class="sxs-lookup"><span data-stu-id="05a52-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="05a52-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="05a52-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="05a52-113">Начало создания материалов Azure с переданным именем и возврат задания asR, используемой для отслеживания операции создания тканью.</span><span class="sxs-lookup"><span data-stu-id="05a52-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="05a52-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05a52-114">PARAMETERS</span></span>

### <span data-ttu-id="05a52-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="05a52-115">-Azure</span></span>
<span data-ttu-id="05a52-116">Параметр переключения определяет создание azure fabric.</span><span class="sxs-lookup"><span data-stu-id="05a52-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a52-117">-DefaultProfile</span></span>
<span data-ttu-id="05a52-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05a52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a52-119">-Location</span><span class="sxs-lookup"><span data-stu-id="05a52-119">-Location</span></span>
<span data-ttu-id="05a52-120">Определяет регион Azure, соответствующий созданному объекту "Ткань".</span><span class="sxs-lookup"><span data-stu-id="05a52-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="05a52-121">Объект "Восстановление сайта Azure" представляет регион.</span><span class="sxs-lookup"><span data-stu-id="05a52-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="05a52-122">Для виртуальных машин, реплицируемых между двумя областями Azure, основной материал представляет основной регион Azure и ткань для восстановления.</span><span class="sxs-lookup"><span data-stu-id="05a52-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a52-123">-Name</span><span class="sxs-lookup"><span data-stu-id="05a52-123">-Name</span></span>
<span data-ttu-id="05a52-124">Указывает имя ткань для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="05a52-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a52-125">-Type</span><span class="sxs-lookup"><span data-stu-id="05a52-125">-Type</span></span>
<span data-ttu-id="05a52-126">Определяет тип ткань для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="05a52-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a52-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05a52-127">-Confirm</span></span>
<span data-ttu-id="05a52-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05a52-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a52-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a52-129">-WhatIf</span></span>
<span data-ttu-id="05a52-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05a52-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05a52-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="05a52-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a52-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a52-132">CommonParameters</span></span>
<span data-ttu-id="05a52-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a52-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a52-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05a52-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a52-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05a52-135">INPUTS</span></span>

### <span data-ttu-id="05a52-136">Нет</span><span class="sxs-lookup"><span data-stu-id="05a52-136">None</span></span>

## <span data-ttu-id="05a52-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05a52-137">OUTPUTS</span></span>

### <span data-ttu-id="05a52-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="05a52-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="05a52-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05a52-139">NOTES</span></span>

## <span data-ttu-id="05a52-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05a52-140">RELATED LINKS</span></span>

[<span data-ttu-id="05a52-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="05a52-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="05a52-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="05a52-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
