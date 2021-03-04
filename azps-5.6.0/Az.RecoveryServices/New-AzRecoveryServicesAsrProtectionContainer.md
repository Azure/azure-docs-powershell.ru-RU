---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 22ade5e749909683ff2de93065ccf458ab2ec73f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956712"
---
# <span data-ttu-id="812ef-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="812ef-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="812ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="812ef-102">SYNOPSIS</span></span>
<span data-ttu-id="812ef-103">Создает контейнер Azure Site Recovery Protection в указанной тканью.</span><span class="sxs-lookup"><span data-stu-id="812ef-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="812ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="812ef-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="812ef-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="812ef-105">DESCRIPTION</span></span>
<span data-ttu-id="812ef-106">С New-AzRecoveryServicesAsrProtectionContainer создается контейнер защиты для указанной тканью для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="812ef-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="812ef-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="812ef-107">EXAMPLES</span></span>

### <span data-ttu-id="812ef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="812ef-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="812ef-109">Запускает контейнер защиты с указанными параметрами и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="812ef-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="812ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="812ef-110">PARAMETERS</span></span>

### <span data-ttu-id="812ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812ef-111">-DefaultProfile</span></span>
<span data-ttu-id="812ef-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="812ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="812ef-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="812ef-113">-InputObject</span></span>
<span data-ttu-id="812ef-114">Создает контейнер защиты репликации в указанном входном объекте (azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="812ef-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="812ef-115">-Name</span><span class="sxs-lookup"><span data-stu-id="812ef-115">-Name</span></span>
<span data-ttu-id="812ef-116">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="812ef-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="812ef-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="812ef-117">-Confirm</span></span>
<span data-ttu-id="812ef-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="812ef-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="812ef-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="812ef-119">-WhatIf</span></span>
<span data-ttu-id="812ef-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="812ef-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="812ef-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="812ef-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="812ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812ef-122">CommonParameters</span></span>
<span data-ttu-id="812ef-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="812ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812ef-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="812ef-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812ef-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="812ef-125">INPUTS</span></span>

### <span data-ttu-id="812ef-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="812ef-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="812ef-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="812ef-127">OUTPUTS</span></span>

### <span data-ttu-id="812ef-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="812ef-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="812ef-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="812ef-129">NOTES</span></span>

## <span data-ttu-id="812ef-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="812ef-130">RELATED LINKS</span></span>
