---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageacquisition
schema: 2.0.0
ms.openlocfilehash: 098c268d3894d85efe0e17618b5d7ec46b82b0f2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076845"
---
# <span data-ttu-id="85d5c-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="85d5c-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="85d5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="85d5c-103">Возвращает список приобретения больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="85d5c-103">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="85d5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85d5c-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="85d5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85d5c-105">DESCRIPTION</span></span>
<span data-ttu-id="85d5c-106">Возвращает список приобретения больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="85d5c-106">Returns a list of BLOB acquisitions.</span></span>

## <span data-ttu-id="85d5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85d5c-107">EXAMPLES</span></span>

### <span data-ttu-id="85d5c-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="85d5c-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAcquisition
```

<span data-ttu-id="85d5c-109">Получение списка acquistions больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="85d5c-109">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="85d5c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85d5c-110">PARAMETERS</span></span>

### <span data-ttu-id="85d5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d5c-111">-DefaultProfile</span></span>
<span data-ttu-id="85d5c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85d5c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85d5c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="85d5c-113">-Location</span></span>
<span data-ttu-id="85d5c-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="85d5c-114">Resource location.</span></span>

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

### <span data-ttu-id="85d5c-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85d5c-115">-SubscriptionId</span></span>
<span data-ttu-id="85d5c-116">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="85d5c-116">Subscription Id.</span></span>

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

### <span data-ttu-id="85d5c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d5c-117">CommonParameters</span></span>
<span data-ttu-id="85d5c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85d5c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d5c-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85d5c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d5c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85d5c-120">INPUTS</span></span>

## <span data-ttu-id="85d5c-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85d5c-121">OUTPUTS</span></span>

### <span data-ttu-id="85d5c-122">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IAcquisition</span><span class="sxs-lookup"><span data-stu-id="85d5c-122">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IAcquisition</span></span>



## <span data-ttu-id="85d5c-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="85d5c-123">NOTES</span></span>

## <span data-ttu-id="85d5c-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85d5c-124">RELATED LINKS</span></span>

