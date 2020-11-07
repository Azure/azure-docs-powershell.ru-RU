---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: 669a1beecaed14c0ab0705979188995daaf9d95f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912151"
---
# <span data-ttu-id="d98cb-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d98cb-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="d98cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d98cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d98cb-103">Удаление учетных данных из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d98cb-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="d98cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d98cb-104">SYNTAX</span></span>

### <span data-ttu-id="d98cb-105">ObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d98cb-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98cb-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d98cb-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98cb-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d98cb-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98cb-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d98cb-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d98cb-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d98cb-109">DESCRIPTION</span></span>
<span data-ttu-id="d98cb-110">Командлет Remove-AzADSpCredential можно использовать для удаления ключа учетных данных из субъекта-службы в случае раскрытия или в рамках срока действия ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="d98cb-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="d98cb-111">Субъект-служба определяется путем указания либо идентификатора объекта, либо имени субъекта-службы (SPN).</span><span class="sxs-lookup"><span data-stu-id="d98cb-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="d98cb-112">Учетные данные, которые нужно удалить, определяются с помощью идентификатора ключа, если необходимо удалить индивидуальные учетные данные или с помощью переключателя "все" для удаления всех учетных данных, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="d98cb-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="d98cb-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d98cb-113">EXAMPLES</span></span>

### <span data-ttu-id="d98cb-114">Пример 1: удаление определенных учетных данных из субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="d98cb-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="d98cb-115">Удаляет учетные данные с ИД ключа "9044423a-60a3-45AC-9ab1-09534157ebb" из субъекта-службы с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="d98cb-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="d98cb-116">Пример 2. Удаление всех учетных данных для субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="d98cb-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="d98cb-117">Удаляет все учетные данные субъекта-службы с SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="d98cb-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="d98cb-118">Пример 3. Удалите все учетные данные для субъекта-службы с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="d98cb-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="d98cb-119">Возвращает субъекта-службы с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" и каналами, которые должны быть связаны с командлетом Remove-AzADSpCredential, чтобы удалить все учетные данные для этого субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d98cb-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="d98cb-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d98cb-120">PARAMETERS</span></span>

### <span data-ttu-id="d98cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98cb-121">-DefaultProfile</span></span>
<span data-ttu-id="d98cb-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d98cb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d98cb-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d98cb-123">-DisplayName</span></span>
<span data-ttu-id="d98cb-124">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d98cb-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d98cb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d98cb-125">-Force</span></span>
<span data-ttu-id="d98cb-126">Переключиться в режим удаления учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d98cb-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98cb-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="d98cb-127">-KeyId</span></span>
<span data-ttu-id="d98cb-128">Указывает ключ учетных данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d98cb-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="d98cb-129">Идентификаторы ключей для субъекта-службы можно получить с помощью командлета Get-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="d98cb-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d98cb-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d98cb-130">-ObjectId</span></span>
<span data-ttu-id="d98cb-131">Идентификатор объекта субъекта-службы, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d98cb-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d98cb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d98cb-132">-PassThru</span></span>
<span data-ttu-id="d98cb-133">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d98cb-133">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98cb-134">-Намерено</span><span class="sxs-lookup"><span data-stu-id="d98cb-134">-ServicePrincipalName</span></span>
<span data-ttu-id="d98cb-135">Имя (SPN) субъекта-службы, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d98cb-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d98cb-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="d98cb-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="d98cb-137">Объект субъекта-службы, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d98cb-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d98cb-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d98cb-138">-Confirm</span></span>
<span data-ttu-id="d98cb-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d98cb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d98cb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d98cb-140">-WhatIf</span></span>
<span data-ttu-id="d98cb-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d98cb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d98cb-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d98cb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d98cb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98cb-143">CommonParameters</span></span>
<span data-ttu-id="d98cb-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d98cb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98cb-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d98cb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98cb-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d98cb-146">INPUTS</span></span>

### <span data-ttu-id="d98cb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d98cb-147">System.String</span></span>

### <span data-ttu-id="d98cb-148">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d98cb-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="d98cb-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d98cb-149">System.Guid</span></span>

## <span data-ttu-id="d98cb-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d98cb-150">OUTPUTS</span></span>

### <span data-ttu-id="d98cb-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d98cb-151">System.Boolean</span></span>

## <span data-ttu-id="d98cb-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="d98cb-152">NOTES</span></span>

## <span data-ttu-id="d98cb-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d98cb-153">RELATED LINKS</span></span>

[<span data-ttu-id="d98cb-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d98cb-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="d98cb-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d98cb-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="d98cb-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d98cb-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

