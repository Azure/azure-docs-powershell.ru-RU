---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 73d57e6e73b0e7e84dd3fb8bfff04ac8705bd108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733562"
---
# <span data-ttu-id="68e9c-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="68e9c-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="68e9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="68e9c-103">Создает контейнер защиты Azure Site Recovery в указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="68e9c-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68e9c-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="68e9c-106">Командлет New-AzureRmRecoveryServicesAsrProtectionContainer создает контейнер защиты в указанной структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="68e9c-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="68e9c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68e9c-107">EXAMPLES</span></span>

### <span data-ttu-id="68e9c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="68e9c-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="68e9c-109">Запускает создание контейнера защиты с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="68e9c-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="68e9c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68e9c-110">PARAMETERS</span></span>

### <span data-ttu-id="68e9c-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68e9c-111">-Confirm</span></span>
<span data-ttu-id="68e9c-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="68e9c-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e9c-113">-DefaultProfile</span></span>
<span data-ttu-id="68e9c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68e9c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68e9c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68e9c-115">-InputObject</span></span>
<span data-ttu-id="68e9c-116">Создает контейнер защиты репликации в указанном объекте ввода (Microsoft Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="68e9c-116">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68e9c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68e9c-117">-Name</span></span>
<span data-ttu-id="68e9c-118">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="68e9c-118">Name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e9c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e9c-119">-WhatIf</span></span>
<span data-ttu-id="68e9c-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="68e9c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68e9c-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="68e9c-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e9c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e9c-122">CommonParameters</span></span>
<span data-ttu-id="68e9c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68e9c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e9c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e9c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e9c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68e9c-125">INPUTS</span></span>

### <span data-ttu-id="68e9c-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="68e9c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="68e9c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68e9c-127">OUTPUTS</span></span>

### <span data-ttu-id="68e9c-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="68e9c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68e9c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="68e9c-129">NOTES</span></span>

## <span data-ttu-id="68e9c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68e9c-130">RELATED LINKS</span></span>
