---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e4fafb6c1ddc4dda05b6536501f713d04c312172
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729292"
---
# <span data-ttu-id="eaf9e-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="eaf9e-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="eaf9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eaf9e-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf9e-103">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="eaf9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eaf9e-104">SYNTAX</span></span>

### <span data-ttu-id="eaf9e-105">SpObjectIdWithDisplayNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eaf9e-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf9e-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaf9e-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf9e-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaf9e-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf9e-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eaf9e-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf9e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaf9e-109">DESCRIPTION</span></span>
<span data-ttu-id="eaf9e-110">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="eaf9e-111">Чтобы обновить учетные данные, связанные с этим субъектом-службой, используйте командлет New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="eaf9e-112">Чтобы обновить свойства, связанные с основным приложением, используйте командлет Update-AzADApplication.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="eaf9e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eaf9e-113">EXAMPLES</span></span>

### <span data-ttu-id="eaf9e-114">Пример 1. Изменение отображаемого имени субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="eaf9e-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="eaf9e-115">Обновление отображаемого имени субъекта-службы с идентификатором объекта "784136ca-3ae2-4fdd-A388-89d793e7c780" и "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="eaf9e-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="eaf9e-116">Пример 2. Изменение отображаемого имени субъекта-службы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="eaf9e-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="eaf9e-117">Возвращает субъекта-службы с идентификатором объекта "784136ca-3ae2-4fdd-A388-89d793e7c780" и каналами, которые должны использовать командлет Update-AzADServicePrincipal, чтобы изменить отображаемое имя субъекта-службы на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="eaf9e-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="eaf9e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eaf9e-118">PARAMETERS</span></span>

### <span data-ttu-id="eaf9e-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="eaf9e-119">-ApplicationId</span></span>
<span data-ttu-id="eaf9e-120">Идентификатор приложения субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="eaf9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf9e-121">-DefaultProfile</span></span>
<span data-ttu-id="eaf9e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf9e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eaf9e-123">-DisplayName</span></span>
<span data-ttu-id="eaf9e-124">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="eaf9e-125">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="eaf9e-125">-Homepage</span></span>
<span data-ttu-id="eaf9e-126">Главная страница для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="eaf9e-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="eaf9e-127">-IdentifierUri</span></span>
<span data-ttu-id="eaf9e-128">Идентификаторы URI для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="eaf9e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eaf9e-129">-InputObject</span></span>
<span data-ttu-id="eaf9e-130">Объект, представляющий субъект-службу для обновления.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-130">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="eaf9e-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="eaf9e-131">-KeyCredential</span></span>
<span data-ttu-id="eaf9e-132">Учетные данные ключа (-ов) для участника службы.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-132">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="eaf9e-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="eaf9e-133">-ObjectId</span></span>
<span data-ttu-id="eaf9e-134">Идентификатор объекта субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-134">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="eaf9e-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="eaf9e-135">-PasswordCredential</span></span>
<span data-ttu-id="eaf9e-136">Учетные данные пароля для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-136">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="eaf9e-137">-Намерено</span><span class="sxs-lookup"><span data-stu-id="eaf9e-137">-ServicePrincipalName</span></span>
<span data-ttu-id="eaf9e-138">SPN субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="eaf9e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaf9e-139">-Confirm</span></span>
<span data-ttu-id="eaf9e-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf9e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf9e-141">-WhatIf</span></span>
<span data-ttu-id="eaf9e-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf9e-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf9e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf9e-144">CommonParameters</span></span>
<span data-ttu-id="eaf9e-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eaf9e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf9e-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf9e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf9e-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eaf9e-147">INPUTS</span></span>

### <span data-ttu-id="eaf9e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="eaf9e-148">System.String</span></span>

### <span data-ttu-id="eaf9e-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="eaf9e-149">System.Guid</span></span>

### <span data-ttu-id="eaf9e-150">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="eaf9e-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="eaf9e-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaf9e-151">OUTPUTS</span></span>

### <span data-ttu-id="eaf9e-152">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="eaf9e-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="eaf9e-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="eaf9e-153">NOTES</span></span>

## <span data-ttu-id="eaf9e-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaf9e-154">RELATED LINKS</span></span>
