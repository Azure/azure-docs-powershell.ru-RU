---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732182"
---
# <span data-ttu-id="b4bd4-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b4bd4-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="b4bd4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bd4-103">Отключите удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bd4-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4bd4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4bd4-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4bd4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="b4bd4-106">Командлет **Disable-AzureStorageDeleteRetentionPolicy** отключает удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bd4-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b4bd4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4bd4-107">EXAMPLES</span></span>

### <span data-ttu-id="b4bd4-108">Пример 1: Отключение удаления политики хранения для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="b4bd4-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="b4bd4-109">Эта команда отключает удаление политики хранения для службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="b4bd4-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="b4bd4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4bd4-110">PARAMETERS</span></span>

### <span data-ttu-id="b4bd4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b4bd4-111">-Context</span></span>
<span data-ttu-id="b4bd4-112">Объект контекста хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b4bd4-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b4bd4-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4bd4-113">-PassThru</span></span>
<span data-ttu-id="b4bd4-114">Показать DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="b4bd4-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="b4bd4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4bd4-115">-Confirm</span></span>
<span data-ttu-id="b4bd4-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4bd4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4bd4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bd4-117">-WhatIf</span></span>
<span data-ttu-id="b4bd4-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4bd4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bd4-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4bd4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4bd4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bd4-120">CommonParameters</span></span>
<span data-ttu-id="b4bd4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4bd4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bd4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bd4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bd4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4bd4-123">INPUTS</span></span>

### <span data-ttu-id="b4bd4-124">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b4bd4-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b4bd4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4bd4-125">OUTPUTS</span></span>

### <span data-ttu-id="b4bd4-126">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceMode. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="b4bd4-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="b4bd4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4bd4-127">NOTES</span></span>

## <span data-ttu-id="b4bd4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4bd4-128">RELATED LINKS</span></span>

