---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 19d8c4e3a47f7b75073d0207d000b8f18a5c0f6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066165"
---
# <span data-ttu-id="6797f-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6797f-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="6797f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6797f-102">SYNOPSIS</span></span>
<span data-ttu-id="6797f-103">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6797f-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="6797f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6797f-104">SYNTAX</span></span>

### <span data-ttu-id="6797f-105">SpObjectIdWithDisplayNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6797f-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6797f-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6797f-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6797f-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6797f-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6797f-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6797f-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6797f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6797f-109">DESCRIPTION</span></span>
<span data-ttu-id="6797f-110">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6797f-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="6797f-111">Чтобы обновить учетные данные, связанные с этим субъектом-службой, используйте командлет New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="6797f-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="6797f-112">Чтобы обновить свойства, связанные с основным приложением, используйте командлет Update-AzADApplication.</span><span class="sxs-lookup"><span data-stu-id="6797f-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="6797f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6797f-113">EXAMPLES</span></span>

### <span data-ttu-id="6797f-114">Пример 1. Изменение отображаемого имени субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="6797f-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="6797f-115">Обновление отображаемого имени субъекта-службы с идентификатором объекта "784136ca-3ae2-4fdd-A388-89d793e7c780" и "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="6797f-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="6797f-116">Пример 2. Изменение отображаемого имени субъекта-службы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="6797f-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="6797f-117">Возвращает субъекта-службы с идентификатором объекта "784136ca-3ae2-4fdd-A388-89d793e7c780" и каналами, которые должны использовать командлет Update-AzADServicePrincipal, чтобы изменить отображаемое имя субъекта-службы на "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="6797f-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="6797f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6797f-118">PARAMETERS</span></span>

### <span data-ttu-id="6797f-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6797f-119">-ApplicationId</span></span>
<span data-ttu-id="6797f-120">Идентификатор приложения субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="6797f-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="6797f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6797f-121">-DefaultProfile</span></span>
<span data-ttu-id="6797f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6797f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6797f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6797f-123">-DisplayName</span></span>
<span data-ttu-id="6797f-124">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="6797f-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="6797f-125">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="6797f-125">-Homepage</span></span>
<span data-ttu-id="6797f-126">Главная страница для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="6797f-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="6797f-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="6797f-127">-IdentifierUri</span></span>
<span data-ttu-id="6797f-128">Идентификаторы URI для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="6797f-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="6797f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6797f-129">-InputObject</span></span>
<span data-ttu-id="6797f-130">Объект, представляющий субъект-службу для обновления.</span><span class="sxs-lookup"><span data-stu-id="6797f-130">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="6797f-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="6797f-131">-KeyCredential</span></span>
<span data-ttu-id="6797f-132">Учетные данные ключа (-ов) для участника службы.</span><span class="sxs-lookup"><span data-stu-id="6797f-132">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="6797f-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6797f-133">-ObjectId</span></span>
<span data-ttu-id="6797f-134">Идентификатор объекта субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="6797f-134">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="6797f-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="6797f-135">-PasswordCredential</span></span>
<span data-ttu-id="6797f-136">Учетные данные пароля для субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="6797f-136">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="6797f-137">-Намерено</span><span class="sxs-lookup"><span data-stu-id="6797f-137">-ServicePrincipalName</span></span>
<span data-ttu-id="6797f-138">SPN субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="6797f-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="6797f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6797f-139">-Confirm</span></span>
<span data-ttu-id="6797f-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6797f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6797f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6797f-141">-WhatIf</span></span>
<span data-ttu-id="6797f-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6797f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6797f-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6797f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6797f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6797f-144">CommonParameters</span></span>
<span data-ttu-id="6797f-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6797f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6797f-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6797f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6797f-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6797f-147">INPUTS</span></span>

### <span data-ttu-id="6797f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6797f-148">System.String</span></span>

### <span data-ttu-id="6797f-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6797f-149">System.Guid</span></span>

### <span data-ttu-id="6797f-150">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6797f-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="6797f-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6797f-151">OUTPUTS</span></span>

### <span data-ttu-id="6797f-152">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6797f-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="6797f-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="6797f-153">NOTES</span></span>

## <span data-ttu-id="6797f-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6797f-154">RELATED LINKS</span></span>
