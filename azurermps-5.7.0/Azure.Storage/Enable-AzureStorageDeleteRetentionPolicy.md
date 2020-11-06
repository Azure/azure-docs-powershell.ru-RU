---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559407"
---
# <span data-ttu-id="4b61d-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4b61d-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="4b61d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b61d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b61d-103">Включите удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4b61d-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b61d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b61d-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b61d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b61d-105">DESCRIPTION</span></span>
<span data-ttu-id="4b61d-106">Командлет **Enable-AzureStorageDeleteRetentionPolicy** включает удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4b61d-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="4b61d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b61d-107">EXAMPLES</span></span>

### <span data-ttu-id="4b61d-108">Пример 1: Включение удаления политики хранения для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="4b61d-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="4b61d-109">Эта команда включает удаление политики хранения для службы больших двоичных объектов и присвойте удаленным дням хранения BLOB-данных значение 3.</span><span class="sxs-lookup"><span data-stu-id="4b61d-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="4b61d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b61d-110">PARAMETERS</span></span>

### <span data-ttu-id="4b61d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4b61d-111">-Context</span></span>
<span data-ttu-id="4b61d-112">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="4b61d-112">Azure Storage Context Object</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b61d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b61d-113">-PassThru</span></span>
<span data-ttu-id="4b61d-114">Показать DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="4b61d-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="4b61d-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="4b61d-115">-RetentionDays</span></span>
<span data-ttu-id="4b61d-116">Задает количество дней хранения для DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="4b61d-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b61d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b61d-117">-Confirm</span></span>
<span data-ttu-id="4b61d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b61d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b61d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b61d-119">-WhatIf</span></span>
<span data-ttu-id="4b61d-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b61d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b61d-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b61d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b61d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b61d-122">CommonParameters</span></span>
<span data-ttu-id="4b61d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b61d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b61d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b61d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b61d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b61d-125">INPUTS</span></span>

### <span data-ttu-id="4b61d-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b61d-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4b61d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b61d-127">OUTPUTS</span></span>

### <span data-ttu-id="4b61d-128">Microsoft. WindowsAzure. Storage. Shared. Protocol. DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="4b61d-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="4b61d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b61d-129">NOTES</span></span>

## <span data-ttu-id="4b61d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b61d-130">RELATED LINKS</span></span>

