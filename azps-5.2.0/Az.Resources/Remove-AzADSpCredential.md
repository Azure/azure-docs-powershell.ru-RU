---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: bcb33f87b85eb6ad5bce9ba812ebccb4d154e920
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412495"
---
# <span data-ttu-id="123d4-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="123d4-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="123d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123d4-102">SYNOPSIS</span></span>
<span data-ttu-id="123d4-103">Удаляет учетные данные для основной службы.</span><span class="sxs-lookup"><span data-stu-id="123d4-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="123d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="123d4-104">SYNTAX</span></span>

### <span data-ttu-id="123d4-105">ObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="123d4-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="123d4-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="123d4-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="123d4-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="123d4-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="123d4-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="123d4-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="123d4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="123d4-109">DESCRIPTION</span></span>
<span data-ttu-id="123d4-110">Этот Remove-AzADSpCredential можно использовать для удаления ключа учетных данных из ключевого ключа службы в случае компрометации или при истечении срока действия ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="123d4-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="123d4-111">Это имя можно определить по ИД объекта или основной службе (SPN).</span><span class="sxs-lookup"><span data-stu-id="123d4-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="123d4-112">Удаляемая учетная запись будет определена по его ключевому удостоверению, если требуется удалить отдельные учетные данные или использовать переключатель "Все", чтобы удалить все учетные данные, связанные с главой службы.</span><span class="sxs-lookup"><span data-stu-id="123d4-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="123d4-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="123d4-113">EXAMPLES</span></span>

### <span data-ttu-id="123d4-114">Пример 1. Удаление определенных учетных данных для основной службы</span><span class="sxs-lookup"><span data-stu-id="123d4-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="123d4-115">Удаляет учетные данные с помощью ключа "9044423a-60a3-45ac-9ab1-09534157ebb" из-за объекта id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="123d4-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="123d4-116">Пример 2. Удаление всех учетных данных для основной службы</span><span class="sxs-lookup"><span data-stu-id="123d4-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="123d4-117">Удаляет все учетные данные для основного обслуживания с помощью spN http://test123 " ".</span><span class="sxs-lookup"><span data-stu-id="123d4-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="123d4-118">Пример 3. Удаление всех учетных данных для основной услуги с помощью piping</span><span class="sxs-lookup"><span data-stu-id="123d4-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="123d4-119">Получает главную службу с ид объекта '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' и вертами к Remove-AzADSpCredential, чтобы удалить все учетные данные этого основного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="123d4-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="123d4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="123d4-120">PARAMETERS</span></span>

### <span data-ttu-id="123d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123d4-121">-DefaultProfile</span></span>
<span data-ttu-id="123d4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="123d4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="123d4-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="123d4-123">-DisplayName</span></span>
<span data-ttu-id="123d4-124">Отображаемая имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="123d4-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="123d4-125">-Force</span><span class="sxs-lookup"><span data-stu-id="123d4-125">-Force</span></span>
<span data-ttu-id="123d4-126">Переключение на удаление учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="123d4-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="123d4-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="123d4-127">-KeyId</span></span>
<span data-ttu-id="123d4-128">Указывает удаляемую клавишу учетных данных.</span><span class="sxs-lookup"><span data-stu-id="123d4-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="123d4-129">Коды ключей для основной услуги можно получить с помощью Get-AzADSpCredential-управления.</span><span class="sxs-lookup"><span data-stu-id="123d4-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="123d4-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="123d4-130">-ObjectId</span></span>
<span data-ttu-id="123d4-131">Object id of the service principal to remove the credentials from.</span><span class="sxs-lookup"><span data-stu-id="123d4-131">The object id of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="123d4-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="123d4-132">-PassThru</span></span>
<span data-ttu-id="123d4-133">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="123d4-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="123d4-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="123d4-134">-ServicePrincipalName</span></span>
<span data-ttu-id="123d4-135">Имя (SPN) директора-службы, из которого удаляются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="123d4-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="123d4-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="123d4-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="123d4-137">Объект-служба, из который нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="123d4-137">The service principal object to remove the credentials from.</span></span>

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

### <span data-ttu-id="123d4-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="123d4-138">-Confirm</span></span>
<span data-ttu-id="123d4-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="123d4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="123d4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="123d4-140">-WhatIf</span></span>
<span data-ttu-id="123d4-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="123d4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="123d4-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="123d4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="123d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123d4-143">CommonParameters</span></span>
<span data-ttu-id="123d4-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="123d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123d4-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="123d4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123d4-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="123d4-146">INPUTS</span></span>

### <span data-ttu-id="123d4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="123d4-147">System.String</span></span>

### <span data-ttu-id="123d4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="123d4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="123d4-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="123d4-149">System.Guid</span></span>

## <span data-ttu-id="123d4-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="123d4-150">OUTPUTS</span></span>

### <span data-ttu-id="123d4-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="123d4-151">System.Boolean</span></span>

## <span data-ttu-id="123d4-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="123d4-152">NOTES</span></span>

## <span data-ttu-id="123d4-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="123d4-153">RELATED LINKS</span></span>

[<span data-ttu-id="123d4-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="123d4-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="123d4-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="123d4-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="123d4-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="123d4-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

