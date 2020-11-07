---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 9d0fb4f188b3753e22258a27cf8632d85fe866dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914753"
---
# <span data-ttu-id="bfc82-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bfc82-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="bfc82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfc82-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc82-103">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bfc82-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfc82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfc82-104">SYNTAX</span></span>

### <span data-ttu-id="bfc82-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfc82-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfc82-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfc82-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc82-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc82-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc82-121">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc82-121">DESCRIPTION</span></span>
<span data-ttu-id="bfc82-122">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bfc82-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="bfc82-123">Параметр по умолчанию использует значения по умолчанию для параметров, если пользователь не предоставил для них одно значение.</span><span class="sxs-lookup"><span data-stu-id="bfc82-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="bfc82-124">Дополнительные сведения об используемых значениях по умолчанию можно найти в описании указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="bfc82-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="bfc82-125">Этот командлет может назначать роль участнику службы с `Role` параметрами и и `Scope` Параметры; если ни один из этих параметров не указан, роль участника-службы назначена не будет.</span><span class="sxs-lookup"><span data-stu-id="bfc82-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="bfc82-126">Значения по умолчанию для `Role` `Scope` параметров и параметры "участник" и "текущая подписка" соответственно ( _Примечание_. значения по умолчанию используются только в том случае, если пользователь предоставляет значение для одного из двух параметров, но не для другого).</span><span class="sxs-lookup"><span data-stu-id="bfc82-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="bfc82-127">Командлет также неявно создает приложение и задает его свойства (если свойство ApplicationId не задано).</span><span class="sxs-lookup"><span data-stu-id="bfc82-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="bfc82-128">Чтобы обновить параметры, зависящие от приложения, используйте командлет Set-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="bfc82-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="bfc82-129">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfc82-129">EXAMPLES</span></span>

### <span data-ttu-id="bfc82-130">Пример 1: Создание участника простой службы AD</span><span class="sxs-lookup"><span data-stu-id="bfc82-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="bfc82-131">Приведенная выше команда создает участника службы AD, используя значения по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="bfc82-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="bfc82-132">Так как идентификатор приложения не предоставлен, приложение было создано для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bfc82-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="bfc82-133">Так как никаких значений не было предоставлено `Role` или у `Scope` созданного субъекта-службы нет разрешений.</span><span class="sxs-lookup"><span data-stu-id="bfc82-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="bfc82-134">Пример 2-простого создания участника службы AD с указанной ролью и областью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bfc82-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="bfc82-135">Приведенная выше команда создает участника службы AD, используя значения по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="bfc82-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="bfc82-136">Так как идентификатор приложения не предоставлен, приложение было создано для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bfc82-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="bfc82-137">Субъект-служба создан с разрешениями "читатель" на текущую подписку (так как для параметра не было предоставлено значение `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="bfc82-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="bfc82-138">Пример 3-Создание участника службы AD с указанной областью и ролью по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bfc82-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="bfc82-139">Приведенная выше команда создает участника службы AD, используя значения по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="bfc82-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="bfc82-140">Так как идентификатор приложения не предоставлен, приложение было создано для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bfc82-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="bfc82-141">Субъект-служба создан с разрешениями "участник" (так как для параметра не было предоставлено значение `Role` ) для указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfc82-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="bfc82-142">Пример 4: Создание участника службы AD с указанной областью и ролью</span><span class="sxs-lookup"><span data-stu-id="bfc82-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="bfc82-143">Приведенная выше команда создает участника службы AD, используя значения по умолчанию для параметров, которые не указаны.</span><span class="sxs-lookup"><span data-stu-id="bfc82-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="bfc82-144">Так как идентификатор приложения не предоставлен, приложение было создано для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bfc82-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="bfc82-145">Субъект-служба создан с разрешениями "читатель" в указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfc82-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="bfc82-146">Пример 5: Создание участника службы AD с помощью идентификатора приложения с назначением роли</span><span class="sxs-lookup"><span data-stu-id="bfc82-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="bfc82-147">Создание субъекта-службы AD для приложения с идентификатором приложения "34a28ad2-dec4-4a41-bc3b-d22ddf90000e".</span><span class="sxs-lookup"><span data-stu-id="bfc82-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="bfc82-148">Так как никаких значений не было предоставлено `Role` или у `Scope` созданного субъекта-службы нет разрешений.</span><span class="sxs-lookup"><span data-stu-id="bfc82-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="bfc82-149">Пример 6: Создание участника службы AD с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="bfc82-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="bfc82-150">Возвращает приложение с идентификатором объекта "3ede3c26-b443-4e0b-9efc-b05e68338dc3" и каналами, которые можно создать с помощью командлета New-AzureRmADServicePrincipal для создания субъекта-службы AD для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="bfc82-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="bfc82-151">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfc82-151">PARAMETERS</span></span>

### <span data-ttu-id="bfc82-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bfc82-152">-ApplicationId</span></span>
<span data-ttu-id="bfc82-153">Уникальный идентификатор приложения для субъекта-службы в клиенте.</span><span class="sxs-lookup"><span data-stu-id="bfc82-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="bfc82-154">После создания это свойство невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="bfc82-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="bfc82-155">Если идентификатор приложения не указан, будет создан один из них.</span><span class="sxs-lookup"><span data-stu-id="bfc82-155">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="bfc82-156">-ApplicationObject</span></span>
<span data-ttu-id="bfc82-157">Объект, представляющий приложение, для которого создается субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="bfc82-157">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-158">-CertValue</span><span class="sxs-lookup"><span data-stu-id="bfc82-158">-CertValue</span></span>
<span data-ttu-id="bfc82-159">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="bfc82-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="bfc82-160">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="bfc82-160">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc82-161">-DefaultProfile</span></span>
<span data-ttu-id="bfc82-162">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bfc82-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfc82-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bfc82-163">-DisplayName</span></span>
<span data-ttu-id="bfc82-164">Понятное имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bfc82-164">The friendly name of the service principal.</span></span> <span data-ttu-id="bfc82-165">Если отображаемое имя не задано, это значение будет использоваться по умолчанию: "Azure-PowerShell-MM-DD-гггг-чч-мм-СС", где суффикс — это время создания приложения.</span><span class="sxs-lookup"><span data-stu-id="bfc82-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-166">-EndDate</span><span class="sxs-lookup"><span data-stu-id="bfc82-166">-EndDate</span></span>
<span data-ttu-id="bfc82-167">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="bfc82-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="bfc82-168">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="bfc82-168">The default end date value is one year from today.</span></span> <span data-ttu-id="bfc82-169">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="bfc82-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-170">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="bfc82-170">-KeyCredential</span></span>
<span data-ttu-id="bfc82-171">Коллекция ключевых учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="bfc82-171">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-172">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="bfc82-172">-Password</span></span>
<span data-ttu-id="bfc82-173">Пароль, который должен быть связан с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="bfc82-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="bfc82-174">Если пароль не указан, создается случайный идентификатор GUID, который будет использоваться в качестве пароля.</span><span class="sxs-lookup"><span data-stu-id="bfc82-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="bfc82-175">-PasswordCredential</span></span>
<span data-ttu-id="bfc82-176">Коллекция учетных данных пароля, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="bfc82-176">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-177">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="bfc82-177">-Role</span></span>
<span data-ttu-id="bfc82-178">Роль, которую участник службы имеет над областью.</span><span class="sxs-lookup"><span data-stu-id="bfc82-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="bfc82-179">Если задано значение, `Scope` но для него не указано значение `Role` , `Role` по умолчанию будет использоваться роль "участник".</span><span class="sxs-lookup"><span data-stu-id="bfc82-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-180">-Scope</span><span class="sxs-lookup"><span data-stu-id="bfc82-180">-Scope</span></span>
<span data-ttu-id="bfc82-181">Область, для которой предоставлены разрешения субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bfc82-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="bfc82-182">Если задано значение, `Role` но для него не указано значение `Scope` , `Scope` по умолчанию будет использоваться текущая подписка.</span><span class="sxs-lookup"><span data-stu-id="bfc82-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="bfc82-183">-SkipAssignment</span></span>
<span data-ttu-id="bfc82-184">Если задано значение, будет пропущено создание назначения роли по умолчанию для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bfc82-184">If set, will skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-185">-StartDate</span><span class="sxs-lookup"><span data-stu-id="bfc82-185">-StartDate</span></span>
<span data-ttu-id="bfc82-186">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="bfc82-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="bfc82-187">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="bfc82-187">The default start date value is today.</span></span> <span data-ttu-id="bfc82-188">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="bfc82-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfc82-189">-Confirm</span></span>
<span data-ttu-id="bfc82-190">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bfc82-190">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc82-191">-WhatIf</span></span>
<span data-ttu-id="bfc82-192">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bfc82-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfc82-193">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bfc82-193">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc82-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc82-194">CommonParameters</span></span>
<span data-ttu-id="bfc82-195">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfc82-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc82-196">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc82-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc82-197">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfc82-197">INPUTS</span></span>

### <span data-ttu-id="bfc82-198">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bfc82-198">System.Guid</span></span>

### <span data-ttu-id="bfc82-199">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc82-199">System.String</span></span>

### <span data-ttu-id="bfc82-200">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="bfc82-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="bfc82-201">Параметры: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bfc82-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="bfc82-202">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="bfc82-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="bfc82-203">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="bfc82-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="bfc82-204">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="bfc82-204">System.Security.SecureString</span></span>

### <span data-ttu-id="bfc82-205">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bfc82-205">System.DateTime</span></span>

## <span data-ttu-id="bfc82-206">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc82-206">OUTPUTS</span></span>

### <span data-ttu-id="bfc82-207">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bfc82-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="bfc82-208">Microsoft. Azure. Commands. Resources. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="bfc82-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="bfc82-209">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfc82-209">NOTES</span></span>
<span data-ttu-id="bfc82-210">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="bfc82-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="bfc82-211">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfc82-211">RELATED LINKS</span></span>

[<span data-ttu-id="bfc82-212">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bfc82-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="bfc82-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bfc82-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="bfc82-214">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bfc82-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="bfc82-215">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="bfc82-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="bfc82-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="bfc82-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="bfc82-217">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="bfc82-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="bfc82-218">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="bfc82-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

