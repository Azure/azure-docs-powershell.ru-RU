---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236743"
---
# <span data-ttu-id="7091c-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="7091c-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="7091c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7091c-102">SYNOPSIS</span></span>
<span data-ttu-id="7091c-103">Получение приложения.</span><span class="sxs-lookup"><span data-stu-id="7091c-103">Get an application.</span></span>

## <span data-ttu-id="7091c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7091c-104">SYNTAX</span></span>

### <span data-ttu-id="7091c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7091c-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7091c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="7091c-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7091c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7091c-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7091c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7091c-108">DESCRIPTION</span></span>
<span data-ttu-id="7091c-109">Получение приложения.</span><span class="sxs-lookup"><span data-stu-id="7091c-109">Get an application.</span></span>

## <span data-ttu-id="7091c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7091c-110">EXAMPLES</span></span>

### <span data-ttu-id="7091c-111">Пример 1: получение приложения виртуальных рабочих столов Windows по имени</span><span class="sxs-lookup"><span data-stu-id="7091c-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="7091c-112">Эта команда получает приложение виртуальных рабочих столов Windows в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="7091c-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="7091c-113">Пример 2: список приложений виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="7091c-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="7091c-114">Эта команда перечисляет приложения виртуальных рабочих столов Windows в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="7091c-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="7091c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7091c-115">PARAMETERS</span></span>

### <span data-ttu-id="7091c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7091c-116">-DefaultProfile</span></span>
<span data-ttu-id="7091c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7091c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7091c-118">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="7091c-118">-GroupName</span></span>
<span data-ttu-id="7091c-119">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="7091c-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7091c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7091c-120">-InputObject</span></span>
<span data-ttu-id="7091c-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7091c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7091c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7091c-122">-Name</span></span>
<span data-ttu-id="7091c-123">Имя приложения в заданной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="7091c-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7091c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7091c-124">-ResourceGroupName</span></span>
<span data-ttu-id="7091c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7091c-125">The name of the resource group.</span></span>
<span data-ttu-id="7091c-126">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="7091c-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7091c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7091c-127">-SubscriptionId</span></span>
<span data-ttu-id="7091c-128">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="7091c-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7091c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7091c-129">CommonParameters</span></span>
<span data-ttu-id="7091c-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7091c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7091c-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7091c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7091c-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7091c-132">INPUTS</span></span>

### <span data-ttu-id="7091c-133">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="7091c-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="7091c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7091c-134">OUTPUTS</span></span>

### <span data-ttu-id="7091c-135">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="7091c-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="7091c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7091c-136">NOTES</span></span>

<span data-ttu-id="7091c-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="7091c-137">ALIASES</span></span>

<span data-ttu-id="7091c-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7091c-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7091c-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7091c-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7091c-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7091c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7091c-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="7091c-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7091c-142">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="7091c-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="7091c-143">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="7091c-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="7091c-144">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="7091c-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="7091c-145">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7091c-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="7091c-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="7091c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7091c-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7091c-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7091c-148">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="7091c-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="7091c-149">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="7091c-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="7091c-150">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="7091c-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7091c-151">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="7091c-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="7091c-152">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7091c-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="7091c-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7091c-153">RELATED LINKS</span></span>

