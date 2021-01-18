---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: f6344590828663a0cf44d96d6fe733adff8757c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505190"
---
# <span data-ttu-id="06779-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="06779-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="06779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06779-102">SYNOPSIS</span></span>
<span data-ttu-id="06779-103">Удаляет учетные данные из приложения.</span><span class="sxs-lookup"><span data-stu-id="06779-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="06779-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06779-104">SYNTAX</span></span>

### <span data-ttu-id="06779-105">ApplicationObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06779-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06779-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06779-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06779-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06779-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06779-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06779-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06779-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06779-109">DESCRIPTION</span></span>
<span data-ttu-id="06779-110">Этот Remove-AzADAppCredential можно использовать для удаления ключа учетных данных из приложения в случае компрометации или при истечении срока действия ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="06779-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="06779-111">Приложение можно определить по ИД объекта или AppId.</span><span class="sxs-lookup"><span data-stu-id="06779-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="06779-112">Удаляемая учетная данные определена по его ключевому удостоверению.</span><span class="sxs-lookup"><span data-stu-id="06779-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="06779-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06779-113">EXAMPLES</span></span>

### <span data-ttu-id="06779-114">Пример 1. Удаление определенных учетных данных из приложения</span><span class="sxs-lookup"><span data-stu-id="06779-114">Example 1: Remove a specific credential from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="06779-115">Удаляет учетные данные с ключом "9044423a-60a3-45ac-9ab1-09534157ebb" из приложения с ид объекта '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="06779-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="06779-116">Пример 2. Удаление всех учетных данных из приложения</span><span class="sxs-lookup"><span data-stu-id="06779-116">Example 2: Remove all credentials from an application</span></span>

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="06779-117">Удаляет из приложения все учетные данные с ид приложения 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58.'</span><span class="sxs-lookup"><span data-stu-id="06779-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="06779-118">Пример 3. Удаление всех учетных данных с помощью piping</span><span class="sxs-lookup"><span data-stu-id="06779-118">Example 3: Remove all credentials using piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="06779-119">Получает приложение с object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' и вертами, которые до Remove-AzADAppCredential-управления, и удаляет из этого приложения все учетные данные.</span><span class="sxs-lookup"><span data-stu-id="06779-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="06779-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06779-120">PARAMETERS</span></span>

### <span data-ttu-id="06779-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="06779-121">-ApplicationId</span></span>
<span data-ttu-id="06779-122">ИД приложения для удаления учетных данных.</span><span class="sxs-lookup"><span data-stu-id="06779-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06779-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="06779-123">-ApplicationObject</span></span>
<span data-ttu-id="06779-124">Объект приложения, из который нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="06779-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06779-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06779-125">-DefaultProfile</span></span>
<span data-ttu-id="06779-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="06779-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06779-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="06779-127">-DisplayName</span></span>
<span data-ttu-id="06779-128">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="06779-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06779-129">-Force</span><span class="sxs-lookup"><span data-stu-id="06779-129">-Force</span></span>
<span data-ttu-id="06779-130">Переключение на удаление учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="06779-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="06779-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="06779-131">-KeyId</span></span>
<span data-ttu-id="06779-132">Указывает удаляемую клавишу учетных данных.</span><span class="sxs-lookup"><span data-stu-id="06779-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="06779-133">Коды ключей для приложения можно получить с помощью Get-AzADAppCredential-управления.</span><span class="sxs-lookup"><span data-stu-id="06779-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06779-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="06779-134">-ObjectId</span></span>
<span data-ttu-id="06779-135">ИД объекта приложения для удаления учетных данных.</span><span class="sxs-lookup"><span data-stu-id="06779-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06779-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06779-136">-PassThru</span></span>
<span data-ttu-id="06779-137">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="06779-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="06779-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06779-138">-Confirm</span></span>
<span data-ttu-id="06779-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="06779-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06779-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06779-140">-WhatIf</span></span>
<span data-ttu-id="06779-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06779-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06779-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="06779-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06779-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06779-143">CommonParameters</span></span>
<span data-ttu-id="06779-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06779-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06779-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06779-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06779-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06779-146">INPUTS</span></span>

### <span data-ttu-id="06779-147">System.String</span><span class="sxs-lookup"><span data-stu-id="06779-147">System.String</span></span>

### <span data-ttu-id="06779-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="06779-148">System.Guid</span></span>

### <span data-ttu-id="06779-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="06779-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="06779-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06779-150">OUTPUTS</span></span>

### <span data-ttu-id="06779-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06779-151">System.Boolean</span></span>

## <span data-ttu-id="06779-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06779-152">NOTES</span></span>

## <span data-ttu-id="06779-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06779-153">RELATED LINKS</span></span>

[<span data-ttu-id="06779-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="06779-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="06779-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="06779-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="06779-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="06779-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
