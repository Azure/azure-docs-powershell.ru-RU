---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: f7e1f596aef9169a1238f505d39f0dd201dcd8bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214649"
---
# <span data-ttu-id="d17cc-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="d17cc-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="d17cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d17cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d17cc-103">Получить HealthBot.</span><span class="sxs-lookup"><span data-stu-id="d17cc-103">Get a HealthBot.</span></span>

## <span data-ttu-id="d17cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d17cc-104">SYNTAX</span></span>

### <span data-ttu-id="d17cc-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d17cc-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d17cc-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d17cc-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d17cc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d17cc-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d17cc-108">Список</span><span class="sxs-lookup"><span data-stu-id="d17cc-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d17cc-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d17cc-109">DESCRIPTION</span></span>
<span data-ttu-id="d17cc-110">Получить HealthBot.</span><span class="sxs-lookup"><span data-stu-id="d17cc-110">Get a HealthBot.</span></span>

## <span data-ttu-id="d17cc-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d17cc-111">EXAMPLES</span></span>

### <span data-ttu-id="d17cc-112">Пример 1. Получить всех HealthBot</span><span class="sxs-lookup"><span data-stu-id="d17cc-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="d17cc-113">Получить всех HealthBot</span><span class="sxs-lookup"><span data-stu-id="d17cc-113">Get all HealthBot</span></span>

### <span data-ttu-id="d17cc-114">Пример 2. Получить всех HealthBot по ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17cc-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="d17cc-115">Получить всех HealthBot по ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17cc-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="d17cc-116">Пример 3. Получить HealthBot по ResourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="d17cc-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="d17cc-117">Получить HealthBot по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="d17cc-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="d17cc-118">Пример 4. Получить HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="d17cc-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="d17cc-119">Получить HealthBot по InputObject</span><span class="sxs-lookup"><span data-stu-id="d17cc-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="d17cc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d17cc-120">PARAMETERS</span></span>

### <span data-ttu-id="d17cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17cc-121">-DefaultProfile</span></span>
<span data-ttu-id="d17cc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d17cc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d17cc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d17cc-123">-InputObject</span></span>
<span data-ttu-id="d17cc-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d17cc-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d17cc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d17cc-125">-Name</span></span>
<span data-ttu-id="d17cc-126">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="d17cc-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="d17cc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17cc-127">-ResourceGroupName</span></span>
<span data-ttu-id="d17cc-128">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="d17cc-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="d17cc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d17cc-129">-SubscriptionId</span></span>
<span data-ttu-id="d17cc-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d17cc-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d17cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17cc-131">CommonParameters</span></span>
<span data-ttu-id="d17cc-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17cc-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d17cc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17cc-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d17cc-134">INPUTS</span></span>

### <span data-ttu-id="d17cc-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="d17cc-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="d17cc-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d17cc-136">OUTPUTS</span></span>

### <span data-ttu-id="d17cc-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="d17cc-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="d17cc-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d17cc-138">NOTES</span></span>

<span data-ttu-id="d17cc-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d17cc-139">ALIASES</span></span>

<span data-ttu-id="d17cc-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d17cc-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d17cc-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d17cc-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d17cc-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d17cc-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d17cc-143">INPUTOBJECT <IHealthBotIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d17cc-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d17cc-144">`[BotName <String>]`: Название ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="d17cc-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="d17cc-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d17cc-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d17cc-146">`[ResourceGroupName <String>]`: имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="d17cc-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="d17cc-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="d17cc-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d17cc-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d17cc-148">RELATED LINKS</span></span>

