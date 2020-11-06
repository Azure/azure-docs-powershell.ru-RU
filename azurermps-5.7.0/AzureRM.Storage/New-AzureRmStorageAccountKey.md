---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566884"
---
# <span data-ttu-id="63cf2-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="63cf2-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="63cf2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="63cf2-103">Повторное создание ключа хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="63cf2-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63cf2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63cf2-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="63cf2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63cf2-105">DESCRIPTION</span></span>
<span data-ttu-id="63cf2-106">Командлет **New-AzureRmStorageAccountKey** заново создает ключ хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="63cf2-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="63cf2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63cf2-107">EXAMPLES</span></span>

### <span data-ttu-id="63cf2-108">Пример 1: повторное создание ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="63cf2-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="63cf2-109">Эта команда повторно создает ключ хранилища для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="63cf2-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="63cf2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63cf2-110">PARAMETERS</span></span>

### <span data-ttu-id="63cf2-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="63cf2-111">-KeyName</span></span>
<span data-ttu-id="63cf2-112">Указывает, какой ключ нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="63cf2-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="63cf2-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="63cf2-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63cf2-114">key1</span><span class="sxs-lookup"><span data-stu-id="63cf2-114">key1</span></span>
- <span data-ttu-id="63cf2-115">key2</span><span class="sxs-lookup"><span data-stu-id="63cf2-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cf2-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63cf2-116">-Name</span></span>
<span data-ttu-id="63cf2-117">Указывает имя учетной записи хранения, для которой необходимо повторно создать ключ хранилища.</span><span class="sxs-lookup"><span data-stu-id="63cf2-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cf2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63cf2-118">-ResourceGroupName</span></span>
<span data-ttu-id="63cf2-119">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="63cf2-119">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cf2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cf2-120">CommonParameters</span></span>
<span data-ttu-id="63cf2-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63cf2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cf2-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63cf2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cf2-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63cf2-123">INPUTS</span></span>

### <span data-ttu-id="63cf2-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="63cf2-124">None</span></span>
<span data-ttu-id="63cf2-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="63cf2-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63cf2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63cf2-126">OUTPUTS</span></span>

## <span data-ttu-id="63cf2-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="63cf2-127">NOTES</span></span>

## <span data-ttu-id="63cf2-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63cf2-128">RELATED LINKS</span></span>

[<span data-ttu-id="63cf2-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="63cf2-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
