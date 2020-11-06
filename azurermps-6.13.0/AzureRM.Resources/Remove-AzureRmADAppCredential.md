---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 6c076258acd19714f30976fd353d7cbbacdf1d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560687"
---
# <span data-ttu-id="26a5d-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="26a5d-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="26a5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="26a5d-103">Удаление учетных данных из приложения.</span><span class="sxs-lookup"><span data-stu-id="26a5d-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26a5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26a5d-104">SYNTAX</span></span>

### <span data-ttu-id="26a5d-105">ApplicationObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26a5d-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a5d-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26a5d-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a5d-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26a5d-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26a5d-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26a5d-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26a5d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26a5d-109">DESCRIPTION</span></span>
<span data-ttu-id="26a5d-110">Командлет Remove-AzureRmADAppCredential можно использовать для удаления ключа учетных данных из приложения в случае раскрытия или в рамках истечения срока действия смены ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="26a5d-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="26a5d-111">Приложение определяется путем указания идентификатора объекта или AppId.</span><span class="sxs-lookup"><span data-stu-id="26a5d-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="26a5d-112">Удаляемые учетные данные определяются с помощью ее кода ключа.</span><span class="sxs-lookup"><span data-stu-id="26a5d-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="26a5d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26a5d-113">EXAMPLES</span></span>

### <span data-ttu-id="26a5d-114">Пример 1: удаление определенных учетных данных из приложения</span><span class="sxs-lookup"><span data-stu-id="26a5d-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="26a5d-115">Удаляет учетные данные с ИД ключа "9044423a-60a3-45AC-9ab1-09534157ebb" из приложения с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="26a5d-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="26a5d-116">Пример 2. Удаление всех учетных данных из приложения</span><span class="sxs-lookup"><span data-stu-id="26a5d-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="26a5d-117">Удаляет все учетные данные из приложения с идентификатором приложения "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="26a5d-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="26a5d-118">Пример 3. Удаление всех учетных данных с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="26a5d-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADAppCredential
```

<span data-ttu-id="26a5d-119">Возвращает приложение с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" и каналами, которые будут использовать командлет Remove-AzureRmADAppCredential, и удаляет все учетные данные из этого приложения.</span><span class="sxs-lookup"><span data-stu-id="26a5d-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="26a5d-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26a5d-120">PARAMETERS</span></span>

### <span data-ttu-id="26a5d-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="26a5d-121">-ApplicationId</span></span>
<span data-ttu-id="26a5d-122">Идентификатор приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="26a5d-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="26a5d-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="26a5d-123">-ApplicationObject</span></span>
<span data-ttu-id="26a5d-124">Объект приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="26a5d-124">The application object to remove the credentials from.</span></span>

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

### <span data-ttu-id="26a5d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26a5d-125">-DefaultProfile</span></span>
<span data-ttu-id="26a5d-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="26a5d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26a5d-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="26a5d-127">-DisplayName</span></span>
<span data-ttu-id="26a5d-128">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="26a5d-128">The display name of the application.</span></span>

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

### <span data-ttu-id="26a5d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="26a5d-129">-Force</span></span>
<span data-ttu-id="26a5d-130">Переключиться в режим удаления учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="26a5d-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="26a5d-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="26a5d-131">-KeyId</span></span>
<span data-ttu-id="26a5d-132">Указывает ключ учетных данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="26a5d-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="26a5d-133">Коды клавиш для приложения можно получить с помощью командлета Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="26a5d-133">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="26a5d-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="26a5d-134">-ObjectId</span></span>
<span data-ttu-id="26a5d-135">Идентификатор объекта приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="26a5d-135">The object id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="26a5d-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26a5d-136">-PassThru</span></span>
<span data-ttu-id="26a5d-137">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="26a5d-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="26a5d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26a5d-138">-Confirm</span></span>
<span data-ttu-id="26a5d-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26a5d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26a5d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26a5d-140">-WhatIf</span></span>
<span data-ttu-id="26a5d-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26a5d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26a5d-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26a5d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26a5d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a5d-143">CommonParameters</span></span>
<span data-ttu-id="26a5d-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26a5d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a5d-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26a5d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a5d-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26a5d-146">INPUTS</span></span>

### <span data-ttu-id="26a5d-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="26a5d-147">System.Guid</span></span>

### <span data-ttu-id="26a5d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="26a5d-148">System.String</span></span>

### <span data-ttu-id="26a5d-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="26a5d-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="26a5d-150">Параметры: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26a5d-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="26a5d-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26a5d-151">OUTPUTS</span></span>

### <span data-ttu-id="26a5d-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26a5d-152">System.Boolean</span></span>

## <span data-ttu-id="26a5d-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="26a5d-153">NOTES</span></span>

## <span data-ttu-id="26a5d-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26a5d-154">RELATED LINKS</span></span>

[<span data-ttu-id="26a5d-155">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="26a5d-155">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="26a5d-156">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="26a5d-156">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="26a5d-157">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="26a5d-157">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
