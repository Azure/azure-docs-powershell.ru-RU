---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 248cbd6f94a95a0024b9fb72c6a2d8dd896eb0f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905166"
---
# <span data-ttu-id="d48d6-101">New-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d48d6-101">New-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d48d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d48d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d48d6-103">Создает контейнер защиты Azure Site Recovery в указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="d48d6-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

## <span data-ttu-id="d48d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d48d6-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d48d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d48d6-105">DESCRIPTION</span></span>
<span data-ttu-id="d48d6-106">Командлет New-AzRecoveryServicesAsrProtectionContainer создает контейнер защиты в указанной структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="d48d6-106">The New-AzRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="d48d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d48d6-107">EXAMPLES</span></span>

### <span data-ttu-id="d48d6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d48d6-108">Example 1</span></span>
```
PS C:\> $job = New-AzRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="d48d6-109">Запускает создание контейнера защиты с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="d48d6-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d48d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d48d6-110">PARAMETERS</span></span>

### <span data-ttu-id="d48d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d48d6-111">-DefaultProfile</span></span>
<span data-ttu-id="d48d6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d48d6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d48d6-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d48d6-113">-InputObject</span></span>
<span data-ttu-id="d48d6-114">Создает контейнер защиты репликации в указанном объекте ввода (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="d48d6-114">Creates the replication protection container in specified input Object (Azure Fabric).</span></span>

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

### <span data-ttu-id="d48d6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d48d6-115">-Name</span></span>
<span data-ttu-id="d48d6-116">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="d48d6-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="d48d6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d48d6-117">-Confirm</span></span>
<span data-ttu-id="d48d6-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d48d6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d48d6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d48d6-119">-WhatIf</span></span>
<span data-ttu-id="d48d6-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d48d6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d48d6-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d48d6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d48d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48d6-122">CommonParameters</span></span>
<span data-ttu-id="d48d6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d48d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48d6-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d48d6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48d6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d48d6-125">INPUTS</span></span>

### <span data-ttu-id="d48d6-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d48d6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d48d6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d48d6-127">OUTPUTS</span></span>

### <span data-ttu-id="d48d6-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d48d6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d48d6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d48d6-129">NOTES</span></span>

## <span data-ttu-id="d48d6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d48d6-130">RELATED LINKS</span></span>
