---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: e1966e7172bcce724702b8652b5e85fcce79260e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516873"
---
# <span data-ttu-id="df3fc-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="df3fc-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="df3fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="df3fc-103">Создает ткань для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="df3fc-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="df3fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="df3fc-104">SYNTAX</span></span>

### <span data-ttu-id="df3fc-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df3fc-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df3fc-106">Azure</span><span class="sxs-lookup"><span data-stu-id="df3fc-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df3fc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df3fc-107">DESCRIPTION</span></span>
<span data-ttu-id="df3fc-108">Для восстановления сайтов Azure указанного типа создается проектлет **New-AzRecoveryServicesAsrFabric.**</span><span class="sxs-lookup"><span data-stu-id="df3fc-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="df3fc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="df3fc-109">EXAMPLES</span></span>

### <span data-ttu-id="df3fc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df3fc-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="df3fc-111">Начало создания ткань с переданным именем и возврат задания asR, используемой для отслеживания операции создания.</span><span class="sxs-lookup"><span data-stu-id="df3fc-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="df3fc-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df3fc-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="df3fc-113">Начало создания материалов Azure с переданным именем и возврат задания asR, используемой для отслеживания операции создания тканью.</span><span class="sxs-lookup"><span data-stu-id="df3fc-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="df3fc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df3fc-114">PARAMETERS</span></span>

### <span data-ttu-id="df3fc-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="df3fc-115">-Azure</span></span>
<span data-ttu-id="df3fc-116">Параметр переключения определяет создание azure fabric.</span><span class="sxs-lookup"><span data-stu-id="df3fc-116">Switch parameter specifies to create azure fabric.</span></span>

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

### <span data-ttu-id="df3fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df3fc-117">-DefaultProfile</span></span>
<span data-ttu-id="df3fc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df3fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="df3fc-119">-Location</span><span class="sxs-lookup"><span data-stu-id="df3fc-119">-Location</span></span>
<span data-ttu-id="df3fc-120">Определяет регион Azure, соответствующий созданному объекту "Ткань".</span><span class="sxs-lookup"><span data-stu-id="df3fc-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="df3fc-121">Объект "Восстановление сайта Azure" представляет регион.</span><span class="sxs-lookup"><span data-stu-id="df3fc-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="df3fc-122">Для виртуальных машин, реплицируемых между двумя областями Azure, основной материал представляет основной регион Azure и ткань для восстановления.</span><span class="sxs-lookup"><span data-stu-id="df3fc-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="df3fc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="df3fc-123">-Name</span></span>
<span data-ttu-id="df3fc-124">Указывает имя ткань для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="df3fc-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="df3fc-125">-Type</span><span class="sxs-lookup"><span data-stu-id="df3fc-125">-Type</span></span>
<span data-ttu-id="df3fc-126">Определяет тип ткань для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="df3fc-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="df3fc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df3fc-127">-Confirm</span></span>
<span data-ttu-id="df3fc-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df3fc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df3fc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df3fc-129">-WhatIf</span></span>
<span data-ttu-id="df3fc-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df3fc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df3fc-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="df3fc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df3fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df3fc-132">CommonParameters</span></span>
<span data-ttu-id="df3fc-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df3fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df3fc-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df3fc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df3fc-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df3fc-135">INPUTS</span></span>

### <span data-ttu-id="df3fc-136">Нет</span><span class="sxs-lookup"><span data-stu-id="df3fc-136">None</span></span>

## <span data-ttu-id="df3fc-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df3fc-137">OUTPUTS</span></span>

### <span data-ttu-id="df3fc-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="df3fc-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="df3fc-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="df3fc-139">NOTES</span></span>

## <span data-ttu-id="df3fc-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df3fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="df3fc-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="df3fc-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="df3fc-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="df3fc-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
