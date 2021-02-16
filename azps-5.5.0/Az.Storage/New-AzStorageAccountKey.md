---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229825"
---
# <span data-ttu-id="6b0b9-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b0b9-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="6b0b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="6b0b9-103">Повторное сгенерирует ключ хранилища для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6b0b9-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="6b0b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b0b9-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b0b9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b0b9-105">DESCRIPTION</span></span>
<span data-ttu-id="6b0b9-106">Для учетной записи хранилища Azure сгенерирует ключ хранилища с новыми данными **AzStorageAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="6b0b9-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="6b0b9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b0b9-107">EXAMPLES</span></span>

### <span data-ttu-id="6b0b9-108">Пример 1. Повторное сгенерировать ключ хранилища</span><span class="sxs-lookup"><span data-stu-id="6b0b9-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="6b0b9-109">Эта команда повторно сгенерирует ключ хранилища для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6b0b9-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="6b0b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b0b9-110">PARAMETERS</span></span>

### <span data-ttu-id="6b0b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b0b9-111">-DefaultProfile</span></span>
<span data-ttu-id="6b0b9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b0b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b0b9-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6b0b9-113">-KeyName</span></span>
<span data-ttu-id="6b0b9-114">Определяет, какой ключ нужно сгенерировать повторно.</span><span class="sxs-lookup"><span data-stu-id="6b0b9-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="6b0b9-115">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="6b0b9-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b0b9-116">key1</span><span class="sxs-lookup"><span data-stu-id="6b0b9-116">key1</span></span>
- <span data-ttu-id="6b0b9-117">key2</span><span class="sxs-lookup"><span data-stu-id="6b0b9-117">key2</span></span>
- <span data-ttu-id="6b0b9-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="6b0b9-118">kerb1</span></span>
- <span data-ttu-id="6b0b9-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="6b0b9-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0b9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6b0b9-120">-Name</span></span>
<span data-ttu-id="6b0b9-121">Имя учетной записи хранения, для которой нужно сгенерировать ключ хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b0b9-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="6b0b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b0b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b0b9-123">Имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="6b0b9-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="6b0b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b0b9-124">CommonParameters</span></span>
<span data-ttu-id="6b0b9-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b0b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b0b9-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b0b9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b0b9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b0b9-127">INPUTS</span></span>

### <span data-ttu-id="6b0b9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6b0b9-128">System.String</span></span>

## <span data-ttu-id="6b0b9-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b0b9-129">OUTPUTS</span></span>

### <span data-ttu-id="6b0b9-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="6b0b9-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="6b0b9-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b0b9-131">NOTES</span></span>

## <span data-ttu-id="6b0b9-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b0b9-132">RELATED LINKS</span></span>

[<span data-ttu-id="6b0b9-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b0b9-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
