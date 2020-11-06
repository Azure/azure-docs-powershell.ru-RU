---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 14cd1606bc4c8d1709b0ddd64e845a2e84b26df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562264"
---
# <span data-ttu-id="8c216-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8c216-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="8c216-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c216-102">SYNOPSIS</span></span>
<span data-ttu-id="8c216-103">Создание сопоставления классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="8c216-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c216-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c216-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c216-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c216-105">DESCRIPTION</span></span>
<span data-ttu-id="8c216-106">Командлет **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** создает классификацию хранилища для сопоставления хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="8c216-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="8c216-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c216-107">EXAMPLES</span></span>

### <span data-ttu-id="8c216-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8c216-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="8c216-109">Запускает операцию создания сопоставления классификации хранилища с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="8c216-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8c216-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c216-110">PARAMETERS</span></span>

### <span data-ttu-id="8c216-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c216-111">-Name</span></span>
<span data-ttu-id="8c216-112">Задает имя для сопоставления классификаций хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="8c216-112">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="8c216-113">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8c216-113">-PrimaryStorageClassification</span></span>
<span data-ttu-id="8c216-114">Задает основной объект классификации хранилища ASR для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="8c216-114">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c216-115">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8c216-115">-RecoveryStorageClassification</span></span>
<span data-ttu-id="8c216-116">Указывает объект классификации хранилища для восстановления ASR для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="8c216-116">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c216-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c216-117">-Confirm</span></span>
<span data-ttu-id="8c216-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c216-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c216-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c216-119">-WhatIf</span></span>
<span data-ttu-id="8c216-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c216-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c216-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c216-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c216-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c216-122">CommonParameters</span></span>
<span data-ttu-id="8c216-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c216-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c216-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c216-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c216-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c216-125">INPUTS</span></span>

### <span data-ttu-id="8c216-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="8c216-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="8c216-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c216-127">OUTPUTS</span></span>

### <span data-ttu-id="8c216-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8c216-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8c216-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c216-129">NOTES</span></span>

## <span data-ttu-id="8c216-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c216-130">RELATED LINKS</span></span>

[<span data-ttu-id="8c216-131">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8c216-131">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="8c216-132">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="8c216-132">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
