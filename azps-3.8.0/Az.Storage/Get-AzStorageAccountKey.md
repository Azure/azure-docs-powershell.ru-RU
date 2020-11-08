---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: faecfdf62892faba2f7ec1241d7e02daa1e6ed12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066770"
---
# <span data-ttu-id="e1f8a-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e1f8a-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="e1f8a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f8a-103">Получает ключи доступа для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f8a-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="e1f8a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1f8a-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1f8a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f8a-106">Командлет **Get-AzStorageAccountKey** получает ключи доступа для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f8a-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="e1f8a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1f8a-107">EXAMPLES</span></span>

### <span data-ttu-id="e1f8a-108">Пример 1: получение клавиш доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e1f8a-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="e1f8a-109">Эта команда получает ключи для указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f8a-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="e1f8a-110">Пример 2: получение определенного ключа доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e1f8a-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="e1f8a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1f8a-111">PARAMETERS</span></span>

### <span data-ttu-id="e1f8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f8a-112">-DefaultProfile</span></span>
<span data-ttu-id="e1f8a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f8a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f8a-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1f8a-114">-Name</span></span>
<span data-ttu-id="e1f8a-115">Указывает имя учетной записи хранилища, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="e1f8a-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="e1f8a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f8a-116">-ResourceGroupName</span></span>
<span data-ttu-id="e1f8a-117">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="e1f8a-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="e1f8a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f8a-118">CommonParameters</span></span>
<span data-ttu-id="e1f8a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1f8a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f8a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f8a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f8a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1f8a-121">INPUTS</span></span>

### <span data-ttu-id="e1f8a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e1f8a-122">System.String</span></span>

## <span data-ttu-id="e1f8a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f8a-123">OUTPUTS</span></span>

### <span data-ttu-id="e1f8a-124">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e1f8a-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="e1f8a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1f8a-125">NOTES</span></span>

## <span data-ttu-id="e1f8a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1f8a-126">RELATED LINKS</span></span>

[<span data-ttu-id="e1f8a-127">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e1f8a-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


