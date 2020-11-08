---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074704"
---
# <span data-ttu-id="193ab-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="193ab-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="193ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="193ab-102">SYNOPSIS</span></span>
<span data-ttu-id="193ab-103">Создает структуру восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="193ab-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="193ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="193ab-104">SYNTAX</span></span>

### <span data-ttu-id="193ab-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="193ab-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="193ab-106">Служба</span><span class="sxs-lookup"><span data-stu-id="193ab-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="193ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="193ab-107">DESCRIPTION</span></span>
<span data-ttu-id="193ab-108">Командлет **New-AzRecoveryServicesAsrFabric** создает структуру восстановления сайта Azure для указанного типа.</span><span class="sxs-lookup"><span data-stu-id="193ab-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="193ab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="193ab-109">EXAMPLES</span></span>

### <span data-ttu-id="193ab-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="193ab-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="193ab-111">Запускает создание структуры с передаваемым именем и возвращает задание ASR, используемое для отслеживания операции создания структуры.</span><span class="sxs-lookup"><span data-stu-id="193ab-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="193ab-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="193ab-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="193ab-113">Запускает создание структуры Azure с передаваемым именем и возвращает задание ASR, используемое для отслеживания операции создания структуры.</span><span class="sxs-lookup"><span data-stu-id="193ab-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="193ab-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="193ab-114">PARAMETERS</span></span>

### <span data-ttu-id="193ab-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="193ab-115">-Azure</span></span>
<span data-ttu-id="193ab-116">Параметр Switch указывает на необходимость создания Azure Fabric.</span><span class="sxs-lookup"><span data-stu-id="193ab-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="193ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="193ab-117">-DefaultProfile</span></span>
<span data-ttu-id="193ab-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="193ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="193ab-119">-Location</span><span class="sxs-lookup"><span data-stu-id="193ab-119">-Location</span></span>
<span data-ttu-id="193ab-120">Указывает область Azure, соответствующую создаваемому объекту фабрики.</span><span class="sxs-lookup"><span data-stu-id="193ab-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="193ab-121">Объект фабрики восстановления сайта Azure представляет регион.</span><span class="sxs-lookup"><span data-stu-id="193ab-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="193ab-122">Для виртуальных машин, реплицируемых между двумя областями Azure, основная структура представляет первичный регион Azure и структуру восстановления.</span><span class="sxs-lookup"><span data-stu-id="193ab-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="193ab-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="193ab-123">-Name</span></span>
<span data-ttu-id="193ab-124">Указывает имя структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="193ab-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="193ab-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="193ab-125">-Type</span></span>
<span data-ttu-id="193ab-126">Указывает тип структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="193ab-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="193ab-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="193ab-127">-Confirm</span></span>
<span data-ttu-id="193ab-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="193ab-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="193ab-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="193ab-129">-WhatIf</span></span>
<span data-ttu-id="193ab-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="193ab-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="193ab-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="193ab-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="193ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="193ab-132">CommonParameters</span></span>
<span data-ttu-id="193ab-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="193ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="193ab-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="193ab-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="193ab-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="193ab-135">INPUTS</span></span>

### <span data-ttu-id="193ab-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="193ab-136">None</span></span>

## <span data-ttu-id="193ab-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="193ab-137">OUTPUTS</span></span>

### <span data-ttu-id="193ab-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="193ab-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="193ab-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="193ab-139">NOTES</span></span>

## <span data-ttu-id="193ab-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="193ab-140">RELATED LINKS</span></span>

[<span data-ttu-id="193ab-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="193ab-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="193ab-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="193ab-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
