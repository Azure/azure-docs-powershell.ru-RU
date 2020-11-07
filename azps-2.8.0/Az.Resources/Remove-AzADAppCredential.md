---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 5c47e707c3421c6efc1998e55897f6bb9be8fa65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904010"
---
# <span data-ttu-id="8999f-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8999f-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="8999f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8999f-102">SYNOPSIS</span></span>
<span data-ttu-id="8999f-103">Удаление учетных данных из приложения.</span><span class="sxs-lookup"><span data-stu-id="8999f-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="8999f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8999f-104">SYNTAX</span></span>

### <span data-ttu-id="8999f-105">ApplicationObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8999f-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8999f-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8999f-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8999f-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8999f-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8999f-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8999f-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8999f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8999f-109">DESCRIPTION</span></span>
<span data-ttu-id="8999f-110">Командлет Remove-AzADAppCredential можно использовать для удаления ключа учетных данных из приложения в случае раскрытия или в рамках истечения срока действия смены ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="8999f-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="8999f-111">Приложение определяется путем указания идентификатора объекта или AppId.</span><span class="sxs-lookup"><span data-stu-id="8999f-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="8999f-112">Удаляемые учетные данные определяются с помощью ее кода ключа.</span><span class="sxs-lookup"><span data-stu-id="8999f-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="8999f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8999f-113">EXAMPLES</span></span>

### <span data-ttu-id="8999f-114">Пример 1: удаление определенных учетных данных из приложения</span><span class="sxs-lookup"><span data-stu-id="8999f-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="8999f-115">Удаляет учетные данные с ИД ключа "9044423a-60a3-45AC-9ab1-09534157ebb" из приложения с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82".</span><span class="sxs-lookup"><span data-stu-id="8999f-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="8999f-116">Пример 2. Удаление всех учетных данных из приложения</span><span class="sxs-lookup"><span data-stu-id="8999f-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="8999f-117">Удаляет все учетные данные из приложения с идентификатором приложения "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="8999f-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="8999f-118">Пример 3. Удаление всех учетных данных с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="8999f-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="8999f-119">Возвращает приложение с идентификатором объекта "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" и каналами, которые будут использовать командлет Remove-AzADAppCredential, и удаляет все учетные данные из этого приложения.</span><span class="sxs-lookup"><span data-stu-id="8999f-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="8999f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8999f-120">PARAMETERS</span></span>

### <span data-ttu-id="8999f-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8999f-121">-ApplicationId</span></span>
<span data-ttu-id="8999f-122">Идентификатор приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8999f-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="8999f-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="8999f-123">-ApplicationObject</span></span>
<span data-ttu-id="8999f-124">Объект приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8999f-124">The application object to remove the credentials from.</span></span>

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

### <span data-ttu-id="8999f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8999f-125">-DefaultProfile</span></span>
<span data-ttu-id="8999f-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8999f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8999f-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8999f-127">-DisplayName</span></span>
<span data-ttu-id="8999f-128">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="8999f-128">The display name of the application.</span></span>

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

### <span data-ttu-id="8999f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="8999f-129">-Force</span></span>
<span data-ttu-id="8999f-130">Переключиться в режим удаления учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8999f-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="8999f-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="8999f-131">-KeyId</span></span>
<span data-ttu-id="8999f-132">Указывает ключ учетных данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8999f-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="8999f-133">Коды клавиш для приложения можно получить с помощью командлета Get-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="8999f-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="8999f-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8999f-134">-ObjectId</span></span>
<span data-ttu-id="8999f-135">Идентификатор объекта приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8999f-135">The object id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="8999f-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8999f-136">-PassThru</span></span>
<span data-ttu-id="8999f-137">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8999f-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8999f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8999f-138">-Confirm</span></span>
<span data-ttu-id="8999f-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8999f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8999f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8999f-140">-WhatIf</span></span>
<span data-ttu-id="8999f-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8999f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8999f-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8999f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8999f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8999f-143">CommonParameters</span></span>
<span data-ttu-id="8999f-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8999f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8999f-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8999f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8999f-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8999f-146">INPUTS</span></span>

### <span data-ttu-id="8999f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8999f-147">System.String</span></span>

### <span data-ttu-id="8999f-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8999f-148">System.Guid</span></span>

### <span data-ttu-id="8999f-149">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8999f-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8999f-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8999f-150">OUTPUTS</span></span>

### <span data-ttu-id="8999f-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8999f-151">System.Boolean</span></span>

## <span data-ttu-id="8999f-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8999f-152">NOTES</span></span>

## <span data-ttu-id="8999f-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8999f-153">RELATED LINKS</span></span>

[<span data-ttu-id="8999f-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8999f-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="8999f-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8999f-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8999f-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8999f-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
