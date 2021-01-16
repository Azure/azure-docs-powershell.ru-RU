---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404159"
---
# <span data-ttu-id="ab50c-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ab50c-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="ab50c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab50c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab50c-103">Возвращает использование ресурсов хранилища для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ab50c-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="ab50c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab50c-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab50c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab50c-105">DESCRIPTION</span></span>
<span data-ttu-id="ab50c-106">Для текущей подписки можно использовать ресурсы хранилища Azure с использованием **get-AzStorageUsage.**</span><span class="sxs-lookup"><span data-stu-id="ab50c-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="ab50c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab50c-107">EXAMPLES</span></span>

### <span data-ttu-id="ab50c-108">Пример 1. Использование ресурсов хранилища в указанном расположении</span><span class="sxs-lookup"><span data-stu-id="ab50c-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="ab50c-109">Эта команда возвращает использование ресурсов хранилища в указанном расположении по текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="ab50c-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="ab50c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab50c-110">PARAMETERS</span></span>

### <span data-ttu-id="ab50c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab50c-111">-DefaultProfile</span></span>
<span data-ttu-id="ab50c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab50c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab50c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="ab50c-113">-Location</span></span>
<span data-ttu-id="ab50c-114">Указать, что ресурсы хранилища будут заданы в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="ab50c-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="ab50c-115">Если не указано, ресурсы хранилища будут использоваться во всех расположениях, указанных в подписке.</span><span class="sxs-lookup"><span data-stu-id="ab50c-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="ab50c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab50c-116">CommonParameters</span></span>
<span data-ttu-id="ab50c-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab50c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab50c-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab50c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab50c-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab50c-119">INPUTS</span></span>

### <span data-ttu-id="ab50c-120">System.String</span><span class="sxs-lookup"><span data-stu-id="ab50c-120">System.String</span></span>

## <span data-ttu-id="ab50c-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab50c-121">OUTPUTS</span></span>

### <span data-ttu-id="ab50c-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="ab50c-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="ab50c-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab50c-123">NOTES</span></span>

## <span data-ttu-id="ab50c-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab50c-124">RELATED LINKS</span></span>

[<span data-ttu-id="ab50c-125">Azure Storage Manager Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ab50c-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


