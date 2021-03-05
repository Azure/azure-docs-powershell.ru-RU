---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013235"
---
# <span data-ttu-id="45787-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="45787-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="45787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45787-102">SYNOPSIS</span></span>
<span data-ttu-id="45787-103">Получить HealthBot.</span><span class="sxs-lookup"><span data-stu-id="45787-103">Get a HealthBot.</span></span>

## <span data-ttu-id="45787-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45787-104">SYNTAX</span></span>

### <span data-ttu-id="45787-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45787-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45787-106">Получить</span><span class="sxs-lookup"><span data-stu-id="45787-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45787-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45787-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45787-108">Список</span><span class="sxs-lookup"><span data-stu-id="45787-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="45787-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45787-109">DESCRIPTION</span></span>
<span data-ttu-id="45787-110">Получить HealthBot.</span><span class="sxs-lookup"><span data-stu-id="45787-110">Get a HealthBot.</span></span>

## <span data-ttu-id="45787-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45787-111">EXAMPLES</span></span>

### <span data-ttu-id="45787-112">Пример 1. Получить всех HealthBot</span><span class="sxs-lookup"><span data-stu-id="45787-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="45787-113">Получить всех HealthBot</span><span class="sxs-lookup"><span data-stu-id="45787-113">Get all HealthBot</span></span>

### <span data-ttu-id="45787-114">Пример 2. Get all HealthBot by ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45787-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="45787-115">Получить всех HealthBot по ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45787-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="45787-116">Пример 3. Получить HealthBot по ResourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="45787-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="45787-117">Получить HealthBot по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="45787-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="45787-118">Пример 4. Получить HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="45787-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="45787-119">Получить HealthBot по InputObject</span><span class="sxs-lookup"><span data-stu-id="45787-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="45787-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45787-120">PARAMETERS</span></span>

### <span data-ttu-id="45787-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45787-121">-DefaultProfile</span></span>
<span data-ttu-id="45787-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45787-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45787-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45787-123">-InputObject</span></span>
<span data-ttu-id="45787-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="45787-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45787-125">-Name</span><span class="sxs-lookup"><span data-stu-id="45787-125">-Name</span></span>
<span data-ttu-id="45787-126">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="45787-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45787-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45787-127">-ResourceGroupName</span></span>
<span data-ttu-id="45787-128">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="45787-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45787-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45787-129">-SubscriptionId</span></span>
<span data-ttu-id="45787-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="45787-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45787-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45787-131">CommonParameters</span></span>
<span data-ttu-id="45787-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45787-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45787-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45787-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45787-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45787-134">INPUTS</span></span>

### <span data-ttu-id="45787-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="45787-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="45787-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45787-136">OUTPUTS</span></span>

### <span data-ttu-id="45787-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="45787-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="45787-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45787-138">NOTES</span></span>

<span data-ttu-id="45787-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="45787-139">ALIASES</span></span>

<span data-ttu-id="45787-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="45787-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45787-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="45787-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45787-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45787-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45787-143">INPUTOBJECT <IHealthBotIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="45787-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45787-144">`[BotName <String>]`: Название ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="45787-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="45787-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="45787-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45787-146">`[ResourceGroupName <String>]`: имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="45787-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="45787-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="45787-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="45787-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45787-148">RELATED LINKS</span></span>

