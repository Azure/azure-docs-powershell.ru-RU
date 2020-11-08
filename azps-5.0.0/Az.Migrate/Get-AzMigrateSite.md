---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248874"
---
# <span data-ttu-id="387c5-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="387c5-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="387c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="387c5-102">SYNOPSIS</span></span>
<span data-ttu-id="387c5-103">Метод для получения сайта.</span><span class="sxs-lookup"><span data-stu-id="387c5-103">Method to get a site.</span></span>

## <span data-ttu-id="387c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="387c5-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="387c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="387c5-105">DESCRIPTION</span></span>
<span data-ttu-id="387c5-106">Метод для получения сайта.</span><span class="sxs-lookup"><span data-stu-id="387c5-106">Method to get a site.</span></span>

## <span data-ttu-id="387c5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="387c5-107">EXAMPLES</span></span>

### <span data-ttu-id="387c5-108">Пример 1: Get (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="387c5-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="387c5-109">Получение имени сайта</span><span class="sxs-lookup"><span data-stu-id="387c5-109">Get site by name</span></span>

## <span data-ttu-id="387c5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="387c5-110">PARAMETERS</span></span>

### <span data-ttu-id="387c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387c5-111">-DefaultProfile</span></span>
<span data-ttu-id="387c5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="387c5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="387c5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="387c5-113">-Name</span></span>
<span data-ttu-id="387c5-114">Имя сайта.</span><span class="sxs-lookup"><span data-stu-id="387c5-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387c5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387c5-115">-ResourceGroupName</span></span>
<span data-ttu-id="387c5-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="387c5-116">The name of the resource group.</span></span>
<span data-ttu-id="387c5-117">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="387c5-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387c5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="387c5-118">-SubscriptionId</span></span>
<span data-ttu-id="387c5-119">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="387c5-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="387c5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387c5-120">CommonParameters</span></span>
<span data-ttu-id="387c5-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="387c5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387c5-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="387c5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387c5-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="387c5-123">INPUTS</span></span>

## <span data-ttu-id="387c5-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="387c5-124">OUTPUTS</span></span>

### <span data-ttu-id="387c5-125">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api202001. IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="387c5-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="387c5-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="387c5-126">NOTES</span></span>

<span data-ttu-id="387c5-127">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="387c5-127">ALIASES</span></span>

## <span data-ttu-id="387c5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="387c5-128">RELATED LINKS</span></span>

