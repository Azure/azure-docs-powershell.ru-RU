---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5220271538903206876dd8d5c476824e1ac10874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569239"
---
# <span data-ttu-id="ea29d-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ea29d-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="ea29d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea29d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea29d-103">Удаление и Отмена регистрации указанного поставщика служб восстановления Azure Site Recovery из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ea29d-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea29d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea29d-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea29d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea29d-105">DESCRIPTION</span></span>
<span data-ttu-id="ea29d-106">Командлет **Remove-AzureRmRecoveryServicesAsrServicesProvider** удаляет из хранилища указанный поставщик служб восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ea29d-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="ea29d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea29d-107">EXAMPLES</span></span>

### <span data-ttu-id="ea29d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea29d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="ea29d-109">Запускает удаление и отмену регистрации указанного поставщика служб Azure Site Recovery и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="ea29d-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ea29d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea29d-110">PARAMETERS</span></span>

### <span data-ttu-id="ea29d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ea29d-111">-Force</span></span>
<span data-ttu-id="ea29d-112">Принудительное выполнение команды без дополнительных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="ea29d-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="ea29d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea29d-113">-InputObject</span></span>
<span data-ttu-id="ea29d-114">Входной объект для командлета: объект поставщика служб восстановления ASR, соответствующий поставщику услуг восстановления ASR, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ea29d-114">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea29d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea29d-115">-Confirm</span></span>
<span data-ttu-id="ea29d-116">Укажите, требуется ли подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ea29d-116">Specify if confirmation is required.</span></span> <span data-ttu-id="ea29d-117">Установите для параметра Confirm значение $false, чтобы пропустить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ea29d-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="ea29d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea29d-118">-WhatIf</span></span>
<span data-ttu-id="ea29d-119">Показывает, что произойдет, если командлет выполняется без фактического выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="ea29d-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="ea29d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea29d-120">CommonParameters</span></span>
<span data-ttu-id="ea29d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea29d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea29d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea29d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea29d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea29d-123">INPUTS</span></span>

### <span data-ttu-id="ea29d-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ea29d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="ea29d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea29d-125">OUTPUTS</span></span>

### <span data-ttu-id="ea29d-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ea29d-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ea29d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea29d-127">NOTES</span></span>

## <span data-ttu-id="ea29d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea29d-128">RELATED LINKS</span></span>

[<span data-ttu-id="ea29d-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ea29d-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="ea29d-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ea29d-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
