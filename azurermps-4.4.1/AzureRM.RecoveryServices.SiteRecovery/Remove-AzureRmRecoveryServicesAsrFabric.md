---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 3f380110359668af5c1b506e1736d3ecc9f39b3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562263"
---
# <span data-ttu-id="d69b4-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d69b4-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="d69b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d69b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d69b4-103">Удаляет указанную структуру восстановления сайта Azure из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d69b4-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d69b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d69b4-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d69b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d69b4-105">DESCRIPTION</span></span>
<span data-ttu-id="d69b4-106">Командлет **Remove-AzureRmRecoveryServicesAsrFabric** удаляет указанную структуру восстановления сайта Azure из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d69b4-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="d69b4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d69b4-107">EXAMPLES</span></span>

### <span data-ttu-id="d69b4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d69b4-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="d69b4-109">Запускает удаление указанной структуры и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="d69b4-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d69b4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d69b4-110">PARAMETERS</span></span>

### <span data-ttu-id="d69b4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d69b4-111">-Force</span></span>
<span data-ttu-id="d69b4-112">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="d69b4-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69b4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d69b4-113">-InputObject</span></span>
<span data-ttu-id="d69b4-114">Входной объект для командлета: объект Fabric ASR, соответствующий удаляемой структуре.</span><span class="sxs-lookup"><span data-stu-id="d69b4-114">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="d69b4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d69b4-115">-Confirm</span></span>
<span data-ttu-id="d69b4-116">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d69b4-116">Specify if confirmation is required.</span></span> <span data-ttu-id="d69b4-117">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d69b4-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="d69b4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69b4-118">-WhatIf</span></span>
<span data-ttu-id="d69b4-119">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="d69b4-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="d69b4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69b4-120">CommonParameters</span></span>
<span data-ttu-id="d69b4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d69b4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69b4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d69b4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69b4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d69b4-123">INPUTS</span></span>

### <span data-ttu-id="d69b4-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d69b4-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d69b4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d69b4-125">OUTPUTS</span></span>

### <span data-ttu-id="d69b4-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d69b4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d69b4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d69b4-127">NOTES</span></span>

## <span data-ttu-id="d69b4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d69b4-128">RELATED LINKS</span></span>

[<span data-ttu-id="d69b4-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d69b4-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="d69b4-130">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="d69b4-130">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
