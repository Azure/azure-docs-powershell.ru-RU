---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558752"
---
# <span data-ttu-id="d3cce-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d3cce-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="d3cce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3cce-102">SYNOPSIS</span></span>
<span data-ttu-id="d3cce-103">Получает ключи доступа для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="d3cce-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3cce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3cce-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="d3cce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3cce-105">DESCRIPTION</span></span>
<span data-ttu-id="d3cce-106">Командлет **Get-AzureRmStorageAccountKey** получает ключи доступа для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="d3cce-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="d3cce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3cce-107">EXAMPLES</span></span>

### <span data-ttu-id="d3cce-108">Пример 1: получение клавиш доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d3cce-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="d3cce-109">Эта команда получает ключи для указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="d3cce-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="d3cce-110">Пример 2: получение определенного ключа доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d3cce-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="d3cce-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3cce-111">PARAMETERS</span></span>

### <span data-ttu-id="d3cce-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3cce-112">-Name</span></span>
<span data-ttu-id="d3cce-113">Указывает имя учетной записи хранилища, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="d3cce-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="d3cce-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3cce-114">-ResourceGroupName</span></span>
<span data-ttu-id="d3cce-115">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="d3cce-115">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="d3cce-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3cce-116">CommonParameters</span></span>
<span data-ttu-id="d3cce-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3cce-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3cce-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3cce-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3cce-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3cce-119">INPUTS</span></span>

### <span data-ttu-id="d3cce-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="d3cce-120">None</span></span>
<span data-ttu-id="d3cce-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d3cce-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3cce-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3cce-122">OUTPUTS</span></span>

## <span data-ttu-id="d3cce-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3cce-123">NOTES</span></span>

## <span data-ttu-id="d3cce-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3cce-124">RELATED LINKS</span></span>

[<span data-ttu-id="d3cce-125">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d3cce-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)
