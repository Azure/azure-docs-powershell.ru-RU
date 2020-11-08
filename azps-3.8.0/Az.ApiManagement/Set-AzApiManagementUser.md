---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: a70cc953da853fd07dcee835f5a97a0efd2f6406
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074168"
---
# <span data-ttu-id="81d74-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="81d74-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="81d74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81d74-102">SYNOPSIS</span></span>
<span data-ttu-id="81d74-103">Настройка сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="81d74-103">Sets user details.</span></span>

## <span data-ttu-id="81d74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81d74-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81d74-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d74-105">DESCRIPTION</span></span>
<span data-ttu-id="81d74-106">Командлет **Set-AzApiManagementUser** задает сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="81d74-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="81d74-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81d74-107">EXAMPLES</span></span>

### <span data-ttu-id="81d74-108">Пример 1: изменение пароля пользователя, адреса электронной почты и состояния</span><span class="sxs-lookup"><span data-stu-id="81d74-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="81d74-109">Эта команда задает новый пароль пользователя и адрес электронной почты, а также блокирует пользователя.</span><span class="sxs-lookup"><span data-stu-id="81d74-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="81d74-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81d74-110">PARAMETERS</span></span>

### <span data-ttu-id="81d74-111">-Context</span><span class="sxs-lookup"><span data-stu-id="81d74-111">-Context</span></span>
<span data-ttu-id="81d74-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="81d74-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="81d74-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="81d74-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d74-114">-DefaultProfile</span></span>
<span data-ttu-id="81d74-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81d74-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d74-116">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="81d74-116">-Email</span></span>
<span data-ttu-id="81d74-117">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="81d74-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="81d74-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81d74-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="81d74-119">-FirstName</span></span>
<span data-ttu-id="81d74-120">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="81d74-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="81d74-121">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="81d74-121">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="81d74-122">-LastName</span></span>
<span data-ttu-id="81d74-123">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="81d74-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="81d74-124">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="81d74-124">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-125">-Примечание</span><span class="sxs-lookup"><span data-stu-id="81d74-125">-Note</span></span>
<span data-ttu-id="81d74-126">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="81d74-126">Specifies a note about the user.</span></span>
<span data-ttu-id="81d74-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81d74-127">This parameter is optional.</span></span>
<span data-ttu-id="81d74-128">Значение этого параметра по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="81d74-128">The default value of this parameter is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81d74-129">-PassThru</span></span>
<span data-ttu-id="81d74-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="81d74-130">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-131">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="81d74-131">-Password</span></span>
<span data-ttu-id="81d74-132">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="81d74-132">Specifies the user password.</span></span>
<span data-ttu-id="81d74-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81d74-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-134">-State</span><span class="sxs-lookup"><span data-stu-id="81d74-134">-State</span></span>
<span data-ttu-id="81d74-135">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="81d74-135">Specifies the user state.</span></span>
<span data-ttu-id="81d74-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81d74-136">This parameter is optional.</span></span>
<span data-ttu-id="81d74-137">Значение по умолчанию — активна.</span><span class="sxs-lookup"><span data-stu-id="81d74-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="81d74-138">-UserId</span></span>
<span data-ttu-id="81d74-139">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="81d74-139">Specifies the user ID.</span></span>
<span data-ttu-id="81d74-140">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="81d74-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81d74-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81d74-141">-Confirm</span></span>
<span data-ttu-id="81d74-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81d74-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d74-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d74-143">-WhatIf</span></span>
<span data-ttu-id="81d74-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81d74-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81d74-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81d74-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d74-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d74-146">CommonParameters</span></span>
<span data-ttu-id="81d74-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81d74-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d74-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81d74-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d74-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81d74-149">INPUTS</span></span>

### <span data-ttu-id="81d74-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="81d74-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="81d74-151">System. String</span><span class="sxs-lookup"><span data-stu-id="81d74-151">System.String</span></span>

### <span data-ttu-id="81d74-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="81d74-152">System.Security.SecureString</span></span>

### <span data-ttu-id="81d74-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="81d74-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="81d74-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81d74-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81d74-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d74-155">OUTPUTS</span></span>

### <span data-ttu-id="81d74-156">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="81d74-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="81d74-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="81d74-157">NOTES</span></span>

## <span data-ttu-id="81d74-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81d74-158">RELATED LINKS</span></span>

[<span data-ttu-id="81d74-159">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="81d74-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="81d74-160">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="81d74-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="81d74-161">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="81d74-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


