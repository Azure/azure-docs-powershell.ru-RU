---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADServicePrincipal.md
ms.openlocfilehash: ce778da76b0dfc81a8438bdd0fdc3e0a20215843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569739"
---
# <span data-ttu-id="0f386-101">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0f386-101">Update-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="0f386-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f386-102">SYNOPSIS</span></span>
<span data-ttu-id="0f386-103">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0f386-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f386-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f386-104">SYNTAX</span></span>

### <span data-ttu-id="0f386-105">SpObjectIdWithDisplayNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f386-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzureRmADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f386-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f386-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f386-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f386-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f386-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f386-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f386-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f386-109">DESCRIPTION</span></span>
<span data-ttu-id="0f386-110">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0f386-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="0f386-111">Чтобы обновить учетные данные, связанные с этим субъектом-службой, используйте командлет New-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="0f386-111">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="0f386-112">Чтобы обновить свойства, связанные с основным приложением, используйте командлет Update-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="0f386-112">To update the properties associated with the underlying application, please use Update-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="0f386-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f386-113">EXAMPLES</span></span>

### <span data-ttu-id="0f386-114">Пример 1. Изменение отображаемого имени субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="0f386-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="0f386-115">Обновление отображаемого имени субъекта-службы с идентификатором объекта "784136ca-3ae2-4fdd-A388-89d793e7c780" и "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="0f386-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="0f386-116">Пример 2. Изменение отображаемого имени субъекта-службы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="0f386-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzureRmADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="0f386-117">Возвращает субъекта-службы с идентификатором объекта "784136ca-3ae2-4fdd-A388-89d793e7c780" и каналами, которые должны использовать командлет Update-AzureRmADServicePrincipal, чтобы изменить отображаемое имя субъекта-службы на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="0f386-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzureRmADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="0f386-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f386-118">PARAMETERS</span></span>

### <span data-ttu-id="0f386-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0f386-119">-ApplicationId</span></span>
<span data-ttu-id="0f386-120">Идентификатор приложения субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="0f386-120">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f386-121">-DefaultProfile</span></span>
<span data-ttu-id="0f386-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f386-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f386-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0f386-123">-DisplayName</span></span>
<span data-ttu-id="0f386-124">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0f386-124">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-125">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="0f386-125">-Homepage</span></span>
<span data-ttu-id="0f386-126">Главная страница для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0f386-126">The homepage for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="0f386-127">-IdentifierUri</span></span>
<span data-ttu-id="0f386-128">Идентификаторы URI для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0f386-128">The identifier URI(s) for the service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f386-129">-InputObject</span></span>
<span data-ttu-id="0f386-130">Объект, представляющий субъект-службу для обновления.</span><span class="sxs-lookup"><span data-stu-id="0f386-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="0f386-131">-KeyCredential</span></span>
<span data-ttu-id="0f386-132">Учетные данные ключа (-ов) для участника службы.</span><span class="sxs-lookup"><span data-stu-id="0f386-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0f386-133">-ObjectId</span></span>
<span data-ttu-id="0f386-134">Идентификатор объекта субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="0f386-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="0f386-135">-PasswordCredential</span></span>
<span data-ttu-id="0f386-136">Учетные данные пароля для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0f386-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-137">-Намерено</span><span class="sxs-lookup"><span data-stu-id="0f386-137">-ServicePrincipalName</span></span>
<span data-ttu-id="0f386-138">SPN субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="0f386-138">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f386-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f386-139">-Confirm</span></span>
<span data-ttu-id="0f386-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f386-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f386-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f386-141">-WhatIf</span></span>
<span data-ttu-id="0f386-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f386-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f386-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f386-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f386-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f386-144">CommonParameters</span></span>
<span data-ttu-id="0f386-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f386-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f386-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f386-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f386-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f386-147">INPUTS</span></span>

### <span data-ttu-id="0f386-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0f386-148">System.Guid</span></span>

### <span data-ttu-id="0f386-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0f386-149">System.String</span></span>

### <span data-ttu-id="0f386-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0f386-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="0f386-151">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f386-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0f386-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f386-152">OUTPUTS</span></span>

### <span data-ttu-id="0f386-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0f386-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="0f386-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f386-154">NOTES</span></span>

## <span data-ttu-id="0f386-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f386-155">RELATED LINKS</span></span>
