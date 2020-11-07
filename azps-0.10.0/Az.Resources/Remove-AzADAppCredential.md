---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 94a6b1ed2d02e3072a23ccc82fc4a49149b2ae2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910873"
---
# <span data-ttu-id="7e2d6-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e2d6-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="7e2d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2d6-103">Удаление учетных данных из приложения.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="7e2d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e2d6-104">SYNTAX</span></span>

### <span data-ttu-id="7e2d6-105">ApplicationObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e2d6-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e2d6-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e2d6-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e2d6-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e2d6-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e2d6-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e2d6-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e2d6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e2d6-109">DESCRIPTION</span></span>
<span data-ttu-id="7e2d6-110">Командлет Remove-AzADAppCredential можно использовать для удаления ключа учетных данных из приложения в случае раскрытия или в рамках истечения срока действия смены ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="7e2d6-111">Приложение определяется путем указания идентификатора объекта или AppId.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="7e2d6-112">Удаляемые учетные данные определяются с помощью ее кода ключа.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="7e2d6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e2d6-113">EXAMPLES</span></span>

### <span data-ttu-id="7e2d6-114">Пример 1: удаление определенных учетных данных из приложения</span><span class="sxs-lookup"><span data-stu-id="7e2d6-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="7e2d6-115">Удаляет учетные данные с ИД ключа "9044423a-60a3-45AC-9ab1-09534157ebb" из приложения с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="7e2d6-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="7e2d6-116">Пример 2. Удаление всех учетных данных из приложения</span><span class="sxs-lookup"><span data-stu-id="7e2d6-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="7e2d6-117">Удаляет все учетные данные из приложения с идентификатором приложения "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="7e2d6-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="7e2d6-118">Пример 3. Удаление всех учетных данных с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="7e2d6-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="7e2d6-119">Возвращает приложение с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" и каналами, которые будут использовать командлет Remove-AzADAppCredential, и удаляет все учетные данные из этого приложения.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="7e2d6-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e2d6-120">PARAMETERS</span></span>

### <span data-ttu-id="7e2d6-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7e2d6-121">-ApplicationId</span></span>
<span data-ttu-id="7e2d6-122">Идентификатор приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="7e2d6-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7e2d6-123">-ApplicationObject</span></span>
<span data-ttu-id="7e2d6-124">Объект приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2d6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e2d6-125">-DefaultProfile</span></span>
<span data-ttu-id="7e2d6-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7e2d6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2d6-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7e2d6-127">-DisplayName</span></span>
<span data-ttu-id="7e2d6-128">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-128">The display name of the application.</span></span>

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

### <span data-ttu-id="7e2d6-129">-Force</span><span class="sxs-lookup"><span data-stu-id="7e2d6-129">-Force</span></span>
<span data-ttu-id="7e2d6-130">Переключиться в режим удаления учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="7e2d6-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7e2d6-131">-KeyId</span></span>
<span data-ttu-id="7e2d6-132">Указывает ключ учетных данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="7e2d6-133">Коды клавиш для приложения можно получить с помощью командлета Get-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="7e2d6-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7e2d6-134">-ObjectId</span></span>
<span data-ttu-id="7e2d6-135">Идентификатор объекта приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2d6-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e2d6-136">-PassThru</span></span>
<span data-ttu-id="7e2d6-137">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7e2d6-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e2d6-138">-Confirm</span></span>
<span data-ttu-id="7e2d6-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e2d6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e2d6-140">-WhatIf</span></span>
<span data-ttu-id="7e2d6-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e2d6-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e2d6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2d6-143">CommonParameters</span></span>
<span data-ttu-id="7e2d6-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e2d6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2d6-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e2d6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2d6-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e2d6-146">INPUTS</span></span>

### <span data-ttu-id="7e2d6-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7e2d6-147">System.Guid</span></span>

### <span data-ttu-id="7e2d6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7e2d6-148">System.String</span></span>

### <span data-ttu-id="7e2d6-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7e2d6-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="7e2d6-150">Параметры: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e2d6-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="7e2d6-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e2d6-151">OUTPUTS</span></span>

### <span data-ttu-id="7e2d6-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e2d6-152">System.Boolean</span></span>

## <span data-ttu-id="7e2d6-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e2d6-153">NOTES</span></span>

## <span data-ttu-id="7e2d6-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e2d6-154">RELATED LINKS</span></span>

[<span data-ttu-id="7e2d6-155">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e2d6-155">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="7e2d6-156">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e2d6-156">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="7e2d6-157">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7e2d6-157">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
