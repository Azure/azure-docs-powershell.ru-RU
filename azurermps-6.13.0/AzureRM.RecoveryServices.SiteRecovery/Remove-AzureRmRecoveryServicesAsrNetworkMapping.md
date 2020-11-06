---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 56c188b6b6e902fffa9cd777d6a5acf3b38cb2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560747"
---
# <span data-ttu-id="944dd-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="944dd-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="944dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="944dd-102">SYNOPSIS</span></span>
<span data-ttu-id="944dd-103">Удаляет указанное сетевое сопоставление ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="944dd-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="944dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="944dd-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="944dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="944dd-105">DESCRIPTION</span></span>
<span data-ttu-id="944dd-106">Командлет **Remove-AzureRmRecoveryServicesAsrNetworkMapping** удаляет указанное сетевое сопоставление ASR.</span><span class="sxs-lookup"><span data-stu-id="944dd-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="944dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="944dd-107">EXAMPLES</span></span>

### <span data-ttu-id="944dd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="944dd-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="944dd-109">Запускает удаление указанного сопоставления сети ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="944dd-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="944dd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="944dd-110">PARAMETERS</span></span>

### <span data-ttu-id="944dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944dd-111">-DefaultProfile</span></span>
<span data-ttu-id="944dd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="944dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="944dd-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="944dd-113">-InputObject</span></span>
<span data-ttu-id="944dd-114">Входной объект для командлета: объект сопоставления ASR, соответствующий сетевому сопоставлению ASR для удаления.</span><span class="sxs-lookup"><span data-stu-id="944dd-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="944dd-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="944dd-115">-Confirm</span></span>
<span data-ttu-id="944dd-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="944dd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="944dd-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="944dd-117">-WhatIf</span></span>
<span data-ttu-id="944dd-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="944dd-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="944dd-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="944dd-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="944dd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944dd-120">CommonParameters</span></span>
<span data-ttu-id="944dd-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="944dd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944dd-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="944dd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944dd-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="944dd-123">INPUTS</span></span>

### <span data-ttu-id="944dd-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="944dd-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="944dd-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="944dd-125">OUTPUTS</span></span>

### <span data-ttu-id="944dd-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="944dd-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="944dd-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="944dd-127">NOTES</span></span>

## <span data-ttu-id="944dd-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="944dd-128">RELATED LINKS</span></span>

[<span data-ttu-id="944dd-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="944dd-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="944dd-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="944dd-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
