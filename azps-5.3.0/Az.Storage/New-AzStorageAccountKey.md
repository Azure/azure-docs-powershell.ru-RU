---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507061"
---
# <span data-ttu-id="6b99d-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b99d-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="6b99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b99d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b99d-103">Повторное сгенерирует ключ хранилища для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6b99d-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="6b99d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b99d-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b99d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b99d-105">DESCRIPTION</span></span>
<span data-ttu-id="6b99d-106">Для учетной записи хранилища Azure сгенерирует ключ хранилища с новыми данными **AzStorageAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="6b99d-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="6b99d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b99d-107">EXAMPLES</span></span>

### <span data-ttu-id="6b99d-108">Пример 1. Повторное сгенерировать ключ хранения</span><span class="sxs-lookup"><span data-stu-id="6b99d-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="6b99d-109">Эта команда повторно сгенерирует ключ хранилища для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6b99d-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="6b99d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b99d-110">PARAMETERS</span></span>

### <span data-ttu-id="6b99d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b99d-111">-DefaultProfile</span></span>
<span data-ttu-id="6b99d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b99d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b99d-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6b99d-113">-KeyName</span></span>
<span data-ttu-id="6b99d-114">Определяет, какой ключ нужно сгенерировать повторно.</span><span class="sxs-lookup"><span data-stu-id="6b99d-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="6b99d-115">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="6b99d-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b99d-116">key1</span><span class="sxs-lookup"><span data-stu-id="6b99d-116">key1</span></span>
- <span data-ttu-id="6b99d-117">key2</span><span class="sxs-lookup"><span data-stu-id="6b99d-117">key2</span></span>
- <span data-ttu-id="6b99d-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="6b99d-118">kerb1</span></span>
- <span data-ttu-id="6b99d-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="6b99d-119">kerb2</span></span>

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

### <span data-ttu-id="6b99d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6b99d-120">-Name</span></span>
<span data-ttu-id="6b99d-121">Имя учетной записи хранения, для которой нужно сгенерировать ключ хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b99d-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="6b99d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b99d-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b99d-123">Имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="6b99d-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="6b99d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b99d-124">CommonParameters</span></span>
<span data-ttu-id="6b99d-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b99d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b99d-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b99d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b99d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b99d-127">INPUTS</span></span>

### <span data-ttu-id="6b99d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6b99d-128">System.String</span></span>

## <span data-ttu-id="6b99d-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b99d-129">OUTPUTS</span></span>

### <span data-ttu-id="6b99d-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="6b99d-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="6b99d-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b99d-131">NOTES</span></span>

## <span data-ttu-id="6b99d-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b99d-132">RELATED LINKS</span></span>

[<span data-ttu-id="6b99d-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b99d-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
