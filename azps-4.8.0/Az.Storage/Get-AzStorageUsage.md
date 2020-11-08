---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243188"
---
# <span data-ttu-id="57483-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="57483-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="57483-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57483-102">SYNOPSIS</span></span>
<span data-ttu-id="57483-103">Получает использование ресурса хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="57483-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="57483-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57483-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57483-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57483-105">DESCRIPTION</span></span>
<span data-ttu-id="57483-106">Командлет **Get-AzStorageUsage** получает сведения об использовании ресурсов службой хранилища Azure для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="57483-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="57483-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57483-107">EXAMPLES</span></span>

### <span data-ttu-id="57483-108">Пример 1: получение использования ресурсов хранилища в указанном расположении</span><span class="sxs-lookup"><span data-stu-id="57483-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="57483-109">Эта команда получает использование ресурсов хранилища в указанном расположении в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="57483-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="57483-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57483-110">PARAMETERS</span></span>

### <span data-ttu-id="57483-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57483-111">-DefaultProfile</span></span>
<span data-ttu-id="57483-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57483-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57483-113">-Location</span><span class="sxs-lookup"><span data-stu-id="57483-113">-Location</span></span>
<span data-ttu-id="57483-114">Укажите, чтобы получать использование ресурсов хранилища в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="57483-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="57483-115">Если не указано, будет выдаваться использование ресурсов хранилища для всех расположений в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="57483-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57483-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57483-116">CommonParameters</span></span>
<span data-ttu-id="57483-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57483-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57483-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57483-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57483-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57483-119">INPUTS</span></span>

### <span data-ttu-id="57483-120">System. String</span><span class="sxs-lookup"><span data-stu-id="57483-120">System.String</span></span>

## <span data-ttu-id="57483-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57483-121">OUTPUTS</span></span>

### <span data-ttu-id="57483-122">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="57483-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="57483-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="57483-123">NOTES</span></span>

## <span data-ttu-id="57483-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57483-124">RELATED LINKS</span></span>

[<span data-ttu-id="57483-125">Командлеты диспетчера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="57483-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


