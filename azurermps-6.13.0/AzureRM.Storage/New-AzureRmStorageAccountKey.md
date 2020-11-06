---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: e44ccbaae730554db35610ff1084e9740e873e53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568834"
---
# <span data-ttu-id="90f31-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="90f31-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="90f31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90f31-102">SYNOPSIS</span></span>
<span data-ttu-id="90f31-103">Повторное создание ключа хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="90f31-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90f31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90f31-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90f31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90f31-105">DESCRIPTION</span></span>
<span data-ttu-id="90f31-106">Командлет **New-AzureRmStorageAccountKey** заново создает ключ хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="90f31-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="90f31-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90f31-107">EXAMPLES</span></span>

### <span data-ttu-id="90f31-108">Пример 1: повторное создание ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="90f31-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="90f31-109">Эта команда повторно создает ключ хранилища для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="90f31-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="90f31-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90f31-110">PARAMETERS</span></span>

### <span data-ttu-id="90f31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f31-111">-DefaultProfile</span></span>
<span data-ttu-id="90f31-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90f31-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90f31-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="90f31-113">-KeyName</span></span>
<span data-ttu-id="90f31-114">Указывает, какой ключ нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="90f31-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="90f31-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="90f31-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90f31-116">key1</span><span class="sxs-lookup"><span data-stu-id="90f31-116">key1</span></span>
- <span data-ttu-id="90f31-117">key2</span><span class="sxs-lookup"><span data-stu-id="90f31-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f31-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90f31-118">-Name</span></span>
<span data-ttu-id="90f31-119">Указывает имя учетной записи хранения, для которой необходимо повторно создать ключ хранилища.</span><span class="sxs-lookup"><span data-stu-id="90f31-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f31-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90f31-120">-ResourceGroupName</span></span>
<span data-ttu-id="90f31-121">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="90f31-121">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f31-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f31-122">CommonParameters</span></span>
<span data-ttu-id="90f31-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90f31-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f31-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90f31-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f31-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90f31-125">INPUTS</span></span>

### <span data-ttu-id="90f31-126">System. String</span><span class="sxs-lookup"><span data-stu-id="90f31-126">System.String</span></span>

## <span data-ttu-id="90f31-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90f31-127">OUTPUTS</span></span>

### <span data-ttu-id="90f31-128">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="90f31-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="90f31-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="90f31-129">NOTES</span></span>

## <span data-ttu-id="90f31-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90f31-130">RELATED LINKS</span></span>

[<span data-ttu-id="90f31-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="90f31-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
