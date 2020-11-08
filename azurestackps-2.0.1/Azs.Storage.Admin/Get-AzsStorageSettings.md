---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 3ad33f83a4e8f96124682bbb189f210f813ead25
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075282"
---
# <span data-ttu-id="cfcde-101">Get-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="cfcde-101">Get-AzsStorageSettings</span></span>

## <span data-ttu-id="cfcde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfcde-102">SYNOPSIS</span></span>
<span data-ttu-id="cfcde-103">Возвращает параметры поставщика ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="cfcde-103">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="cfcde-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfcde-104">SYNTAX</span></span>

```
Get-AzsStorageSettings [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfcde-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfcde-105">DESCRIPTION</span></span>
<span data-ttu-id="cfcde-106">Возвращает параметры поставщика ресурсов хранилища.</span><span class="sxs-lookup"><span data-stu-id="cfcde-106">Returns the storage resource provider settings.</span></span>

## <span data-ttu-id="cfcde-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfcde-107">EXAMPLES</span></span>

### <span data-ttu-id="cfcde-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="cfcde-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageSettings
```

<span data-ttu-id="cfcde-109">Получение параметров хранилища.</span><span class="sxs-lookup"><span data-stu-id="cfcde-109">Get the storage settings.</span></span>

## <span data-ttu-id="cfcde-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfcde-110">PARAMETERS</span></span>

### <span data-ttu-id="cfcde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfcde-111">-DefaultProfile</span></span>
<span data-ttu-id="cfcde-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfcde-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cfcde-113">-Location</span><span class="sxs-lookup"><span data-stu-id="cfcde-113">-Location</span></span>
<span data-ttu-id="cfcde-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="cfcde-114">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cfcde-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cfcde-115">-SubscriptionId</span></span>
<span data-ttu-id="cfcde-116">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="cfcde-116">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cfcde-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfcde-117">CommonParameters</span></span>
<span data-ttu-id="cfcde-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfcde-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfcde-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfcde-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfcde-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfcde-120">INPUTS</span></span>

## <span data-ttu-id="cfcde-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfcde-121">OUTPUTS</span></span>

### <span data-ttu-id="cfcde-122">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="cfcde-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="cfcde-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfcde-123">NOTES</span></span>

## <span data-ttu-id="cfcde-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfcde-124">RELATED LINKS</span></span>

