---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248877"
---
# <span data-ttu-id="b80b9-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="b80b9-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="b80b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b80b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b80b9-103">Метод для получения учетной записи запуска от имени.</span><span class="sxs-lookup"><span data-stu-id="b80b9-103">Method to get run as account.</span></span>

## <span data-ttu-id="b80b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b80b9-104">SYNTAX</span></span>

### <span data-ttu-id="b80b9-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b80b9-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b80b9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b80b9-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b80b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b80b9-107">DESCRIPTION</span></span>
<span data-ttu-id="b80b9-108">Метод для получения учетной записи запуска от имени.</span><span class="sxs-lookup"><span data-stu-id="b80b9-108">Method to get run as account.</span></span>

## <span data-ttu-id="b80b9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b80b9-109">EXAMPLES</span></span>

### <span data-ttu-id="b80b9-110">Пример 1: список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b80b9-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="b80b9-111">Перечислите все учетные записи запуска от имени на сайте.</span><span class="sxs-lookup"><span data-stu-id="b80b9-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="b80b9-112">Пример 2: Get</span><span class="sxs-lookup"><span data-stu-id="b80b9-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="b80b9-113">Получить учетную запись запуска от имени.</span><span class="sxs-lookup"><span data-stu-id="b80b9-113">Get Run as account by name.</span></span>

## <span data-ttu-id="b80b9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b80b9-114">PARAMETERS</span></span>

### <span data-ttu-id="b80b9-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b80b9-115">-AccountName</span></span>
<span data-ttu-id="b80b9-116">Название учетной записи запуска от имени.</span><span class="sxs-lookup"><span data-stu-id="b80b9-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80b9-117">-DefaultProfile</span></span>
<span data-ttu-id="b80b9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b80b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b80b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b80b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="b80b9-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b80b9-120">The name of the resource group.</span></span>
<span data-ttu-id="b80b9-121">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="b80b9-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b80b9-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="b80b9-122">-SiteName</span></span>
<span data-ttu-id="b80b9-123">Имя сайта.</span><span class="sxs-lookup"><span data-stu-id="b80b9-123">Site name.</span></span>

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

### <span data-ttu-id="b80b9-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b80b9-124">-SubscriptionId</span></span>
<span data-ttu-id="b80b9-125">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b80b9-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b80b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80b9-126">CommonParameters</span></span>
<span data-ttu-id="b80b9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b80b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80b9-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b80b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80b9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b80b9-129">INPUTS</span></span>

## <span data-ttu-id="b80b9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b80b9-130">OUTPUTS</span></span>

### <span data-ttu-id="b80b9-131">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api202001. IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="b80b9-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="b80b9-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b80b9-132">NOTES</span></span>

<span data-ttu-id="b80b9-133">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="b80b9-133">ALIASES</span></span>

## <span data-ttu-id="b80b9-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b80b9-134">RELATED LINKS</span></span>

