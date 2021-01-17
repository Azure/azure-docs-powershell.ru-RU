---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419775"
---
# <span data-ttu-id="ad0b1-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ad0b1-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="ad0b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0b1-103">Обновляет существующую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="ad0b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad0b1-104">SYNTAX</span></span>

### <span data-ttu-id="ad0b1-105">SpObjectIdWithDisplayNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad0b1-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad0b1-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad0b1-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad0b1-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad0b1-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad0b1-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad0b1-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad0b1-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad0b1-109">DESCRIPTION</span></span>
<span data-ttu-id="ad0b1-110">Обновляет существующую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="ad0b1-111">Чтобы обновить учетные данные, связанные с этим принципом обслуживания, используйте New-AzADSpCredential-</span><span class="sxs-lookup"><span data-stu-id="ad0b1-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="ad0b1-112">Чтобы обновить свойства, связанные с приложением, используйте Update-AzADApplication-</span><span class="sxs-lookup"><span data-stu-id="ad0b1-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="ad0b1-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad0b1-113">EXAMPLES</span></span>

### <span data-ttu-id="ad0b1-114">Пример 1. Обновление отображаемого имени директора-службы</span><span class="sxs-lookup"><span data-stu-id="ad0b1-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="ad0b1-115">Отображает имя директора-службы с помощью ид объекта "784136ca-3ae2-4fdd-a388-89d793e7c780" на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="ad0b1-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="ad0b1-116">Пример 2. Обновление отображаемого имени основной услуги с помощью piping</span><span class="sxs-lookup"><span data-stu-id="ad0b1-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="ad0b1-117">Получает главную службу с ид объекта '784136ca-3ae2-4fdd-a388-89d793e7c780' и каналами к Update-AzADServicePrincipal, чтобы обновить отображаемого имени директора-службы на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="ad0b1-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="ad0b1-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ad0b1-118">Example 3</span></span>

<span data-ttu-id="ad0b1-119">Обновляет существующую главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="ad0b1-120">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="ad0b1-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="ad0b1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad0b1-121">PARAMETERS</span></span>

### <span data-ttu-id="ad0b1-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ad0b1-122">-ApplicationId</span></span>
<span data-ttu-id="ad0b1-123">ID приложения, который должен обновить основной службы.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="ad0b1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0b1-124">-DefaultProfile</span></span>
<span data-ttu-id="ad0b1-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad0b1-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ad0b1-126">-DisplayName</span></span>
<span data-ttu-id="ad0b1-127">Отображаемая имя для директора-службы.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="ad0b1-128">-Домашняя странице</span><span class="sxs-lookup"><span data-stu-id="ad0b1-128">-Homepage</span></span>
<span data-ttu-id="ad0b1-129">Домашняя странице для директора-службы.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="ad0b1-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="ad0b1-130">-IdentifierUri</span></span>
<span data-ttu-id="ad0b1-131">URI идентификаторов для основной службы.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="ad0b1-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad0b1-132">-InputObject</span></span>
<span data-ttu-id="ad0b1-133">Объект, представляющий главную службу для обновления.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-133">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad0b1-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="ad0b1-134">-KeyCredential</span></span>
<span data-ttu-id="ad0b1-135">Учетные данные ключа для основного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-135">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0b1-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ad0b1-136">-ObjectId</span></span>
<span data-ttu-id="ad0b1-137">Object id of the service principal to update.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-137">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad0b1-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="ad0b1-138">-PasswordCredential</span></span>
<span data-ttu-id="ad0b1-139">Учетные данные для директора службы.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-139">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0b1-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ad0b1-140">-ServicePrincipalName</span></span>
<span data-ttu-id="ad0b1-141">SpN основного обслуживания, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="ad0b1-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad0b1-142">-Confirm</span></span>
<span data-ttu-id="ad0b1-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad0b1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad0b1-144">-WhatIf</span></span>
<span data-ttu-id="ad0b1-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad0b1-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad0b1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0b1-147">CommonParameters</span></span>
<span data-ttu-id="ad0b1-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad0b1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0b1-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad0b1-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0b1-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad0b1-150">INPUTS</span></span>

### <span data-ttu-id="ad0b1-151">System.String</span><span class="sxs-lookup"><span data-stu-id="ad0b1-151">System.String</span></span>

### <span data-ttu-id="ad0b1-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ad0b1-152">System.Guid</span></span>

### <span data-ttu-id="ad0b1-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ad0b1-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ad0b1-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad0b1-154">OUTPUTS</span></span>

### <span data-ttu-id="ad0b1-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ad0b1-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ad0b1-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad0b1-156">NOTES</span></span>

## <span data-ttu-id="ad0b1-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad0b1-157">RELATED LINKS</span></span>