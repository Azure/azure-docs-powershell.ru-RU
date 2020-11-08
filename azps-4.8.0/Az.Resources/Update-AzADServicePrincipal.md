---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 4a4888573199c4fd5f76282fb5c8eb1702911e00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077645"
---
# <span data-ttu-id="2d514-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2d514-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="2d514-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d514-102">SYNOPSIS</span></span>
<span data-ttu-id="2d514-103">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d514-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="2d514-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d514-104">SYNTAX</span></span>

### <span data-ttu-id="2d514-105">SpObjectIdWithDisplayNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d514-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d514-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d514-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d514-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d514-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d514-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d514-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d514-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d514-109">DESCRIPTION</span></span>
<span data-ttu-id="2d514-110">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d514-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="2d514-111">Чтобы обновить учетные данные, связанные с этим субъектом-службой, используйте командлет New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="2d514-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="2d514-112">Чтобы обновить свойства, связанные с основным приложением, используйте командлет Update-AzADApplication.</span><span class="sxs-lookup"><span data-stu-id="2d514-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="2d514-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d514-113">EXAMPLES</span></span>

### <span data-ttu-id="2d514-114">Пример 1: обновление отображаемого имени субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="2d514-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="2d514-115">Обновление отображаемого имени субъекта-службы с идентификатором объекта "784136ca-3ae2-4fdd-A388-89d793e7c780" и "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="2d514-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="2d514-116">Пример 2: обновление отображаемого имени субъекта-службы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="2d514-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="2d514-117">Возвращает субъекта-службы с идентификатором объекта "784136ca-3ae2-4fdd-A388-89d793e7c780" и каналами, которые должны использовать командлет Update-AzADServicePrincipal, чтобы изменить отображаемое имя субъекта-службы на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="2d514-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="2d514-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2d514-118">Example 3</span></span>

<span data-ttu-id="2d514-119">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d514-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="2d514-120">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="2d514-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="2d514-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d514-121">PARAMETERS</span></span>

### <span data-ttu-id="2d514-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2d514-122">-ApplicationId</span></span>
<span data-ttu-id="2d514-123">Идентификатор приложения субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="2d514-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="2d514-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d514-124">-DefaultProfile</span></span>
<span data-ttu-id="2d514-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d514-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d514-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2d514-126">-DisplayName</span></span>
<span data-ttu-id="2d514-127">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2d514-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="2d514-128">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="2d514-128">-Homepage</span></span>
<span data-ttu-id="2d514-129">Главная страница для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2d514-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="2d514-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="2d514-130">-IdentifierUri</span></span>
<span data-ttu-id="2d514-131">Идентификаторы URI для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2d514-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="2d514-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d514-132">-InputObject</span></span>
<span data-ttu-id="2d514-133">Объект, представляющий субъект-службу для обновления.</span><span class="sxs-lookup"><span data-stu-id="2d514-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="2d514-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="2d514-134">-KeyCredential</span></span>
<span data-ttu-id="2d514-135">Учетные данные ключа (-ов) для участника службы.</span><span class="sxs-lookup"><span data-stu-id="2d514-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="2d514-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2d514-136">-ObjectId</span></span>
<span data-ttu-id="2d514-137">Идентификатор объекта субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="2d514-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="2d514-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="2d514-138">-PasswordCredential</span></span>
<span data-ttu-id="2d514-139">Учетные данные пароля для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2d514-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="2d514-140">-Намерено</span><span class="sxs-lookup"><span data-stu-id="2d514-140">-ServicePrincipalName</span></span>
<span data-ttu-id="2d514-141">SPN субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="2d514-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="2d514-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d514-142">-Confirm</span></span>
<span data-ttu-id="2d514-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d514-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d514-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d514-144">-WhatIf</span></span>
<span data-ttu-id="2d514-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d514-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d514-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d514-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d514-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d514-147">CommonParameters</span></span>
<span data-ttu-id="2d514-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d514-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d514-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d514-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d514-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d514-150">INPUTS</span></span>

### <span data-ttu-id="2d514-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2d514-151">System.String</span></span>

### <span data-ttu-id="2d514-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2d514-152">System.Guid</span></span>

### <span data-ttu-id="2d514-153">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2d514-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2d514-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d514-154">OUTPUTS</span></span>

### <span data-ttu-id="2d514-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2d514-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2d514-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d514-156">NOTES</span></span>

## <span data-ttu-id="2d514-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d514-157">RELATED LINKS</span></span>
