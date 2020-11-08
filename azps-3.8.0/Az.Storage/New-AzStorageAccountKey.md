---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: d63c948e59dbc05122c63b6688277a7015a42163
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073145"
---
# <span data-ttu-id="b07a1-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b07a1-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="b07a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b07a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b07a1-103">Повторное создание ключа хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="b07a1-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="b07a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b07a1-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b07a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07a1-105">DESCRIPTION</span></span>
<span data-ttu-id="b07a1-106">Командлет **New-AzStorageAccountKey** заново создает ключ хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="b07a1-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="b07a1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b07a1-107">EXAMPLES</span></span>

### <span data-ttu-id="b07a1-108">Пример 1: повторное создание ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="b07a1-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="b07a1-109">Эта команда повторно создает ключ хранилища для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b07a1-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="b07a1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b07a1-110">PARAMETERS</span></span>

### <span data-ttu-id="b07a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07a1-111">-DefaultProfile</span></span>
<span data-ttu-id="b07a1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b07a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b07a1-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b07a1-113">-KeyName</span></span>
<span data-ttu-id="b07a1-114">Указывает, какой ключ нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="b07a1-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="b07a1-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b07a1-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b07a1-116">key1</span><span class="sxs-lookup"><span data-stu-id="b07a1-116">key1</span></span>
- <span data-ttu-id="b07a1-117">key2</span><span class="sxs-lookup"><span data-stu-id="b07a1-117">key2</span></span>

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

### <span data-ttu-id="b07a1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b07a1-118">-Name</span></span>
<span data-ttu-id="b07a1-119">Указывает имя учетной записи хранения, для которой необходимо повторно создать ключ хранилища.</span><span class="sxs-lookup"><span data-stu-id="b07a1-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="b07a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="b07a1-121">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="b07a1-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="b07a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07a1-122">CommonParameters</span></span>
<span data-ttu-id="b07a1-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b07a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07a1-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07a1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07a1-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b07a1-125">INPUTS</span></span>

### <span data-ttu-id="b07a1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b07a1-126">System.String</span></span>

## <span data-ttu-id="b07a1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07a1-127">OUTPUTS</span></span>

### <span data-ttu-id="b07a1-128">Microsoft. Azure. Management. Storage. Models. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="b07a1-128">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="b07a1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b07a1-129">NOTES</span></span>

## <span data-ttu-id="b07a1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b07a1-130">RELATED LINKS</span></span>

[<span data-ttu-id="b07a1-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b07a1-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
