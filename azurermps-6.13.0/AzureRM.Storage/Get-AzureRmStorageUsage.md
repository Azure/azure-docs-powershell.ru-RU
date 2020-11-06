---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565785"
---
# <span data-ttu-id="1afcf-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1afcf-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="1afcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1afcf-102">SYNOPSIS</span></span>
<span data-ttu-id="1afcf-103">Получает использование ресурса хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="1afcf-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1afcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1afcf-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1afcf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1afcf-105">DESCRIPTION</span></span>
<span data-ttu-id="1afcf-106">Командлет **Get-AzureRmStorageUsage** получает сведения об использовании ресурсов службой хранилища Azure для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="1afcf-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="1afcf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1afcf-107">EXAMPLES</span></span>

### <span data-ttu-id="1afcf-108">Пример 1: получение сведений об использовании ресурсов хранилища</span><span class="sxs-lookup"><span data-stu-id="1afcf-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="1afcf-109">Эта команда получает использование ресурсов хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="1afcf-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="1afcf-110">Пример 2: получение использования ресурсов хранилища в указанном расположении</span><span class="sxs-lookup"><span data-stu-id="1afcf-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="1afcf-111">Эта команда получает использование ресурсов хранилища в указанном расположении в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="1afcf-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="1afcf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1afcf-112">PARAMETERS</span></span>

### <span data-ttu-id="1afcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afcf-113">-DefaultProfile</span></span>
<span data-ttu-id="1afcf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1afcf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1afcf-115">-Location</span><span class="sxs-lookup"><span data-stu-id="1afcf-115">-Location</span></span>
<span data-ttu-id="1afcf-116">Укажите, чтобы получать использование ресурсов хранилища в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="1afcf-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="1afcf-117">Если не указано, будет выдаваться использование ресурсов хранилища для всех расположений в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="1afcf-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afcf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afcf-118">CommonParameters</span></span>
<span data-ttu-id="1afcf-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1afcf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afcf-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1afcf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afcf-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1afcf-121">INPUTS</span></span>

### <span data-ttu-id="1afcf-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="1afcf-122">None</span></span>

## <span data-ttu-id="1afcf-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1afcf-123">OUTPUTS</span></span>

### <span data-ttu-id="1afcf-124">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="1afcf-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="1afcf-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1afcf-125">NOTES</span></span>

## <span data-ttu-id="1afcf-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1afcf-126">RELATED LINKS</span></span>

[<span data-ttu-id="1afcf-127">Командлеты диспетчера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="1afcf-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


