---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: ccd19f0390957466f9fb799d3655aa8bb1d02d68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727919"
---
# <span data-ttu-id="54972-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54972-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="54972-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54972-102">SYNOPSIS</span></span>
<span data-ttu-id="54972-103">Настройка сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="54972-103">Sets user details.</span></span>

## <span data-ttu-id="54972-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54972-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54972-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54972-105">DESCRIPTION</span></span>
<span data-ttu-id="54972-106">Командлет **Set-AzApiManagementUser** задает сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="54972-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="54972-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54972-107">EXAMPLES</span></span>

### <span data-ttu-id="54972-108">Пример 1: изменение пароля пользователя, адреса электронной почты и состояния</span><span class="sxs-lookup"><span data-stu-id="54972-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="54972-109">Эта команда задает новый пароль пользователя и адрес электронной почты, а также блокирует пользователя.</span><span class="sxs-lookup"><span data-stu-id="54972-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="54972-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54972-110">PARAMETERS</span></span>

### <span data-ttu-id="54972-111">-Context</span><span class="sxs-lookup"><span data-stu-id="54972-111">-Context</span></span>
<span data-ttu-id="54972-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="54972-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="54972-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="54972-113">This parameter is required.</span></span>

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

### <span data-ttu-id="54972-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54972-114">-DefaultProfile</span></span>
<span data-ttu-id="54972-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54972-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54972-116">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="54972-116">-Email</span></span>
<span data-ttu-id="54972-117">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="54972-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="54972-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="54972-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="54972-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="54972-119">-FirstName</span></span>
<span data-ttu-id="54972-120">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="54972-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="54972-121">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="54972-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="54972-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="54972-122">-LastName</span></span>
<span data-ttu-id="54972-123">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="54972-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="54972-124">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="54972-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="54972-125">-Примечание</span><span class="sxs-lookup"><span data-stu-id="54972-125">-Note</span></span>
<span data-ttu-id="54972-126">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="54972-126">Specifies a note about the user.</span></span>
<span data-ttu-id="54972-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="54972-127">This parameter is optional.</span></span>
<span data-ttu-id="54972-128">Значение этого параметра по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="54972-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="54972-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54972-129">-PassThru</span></span>
<span data-ttu-id="54972-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="54972-130">passthru</span></span>

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

### <span data-ttu-id="54972-131">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="54972-131">-Password</span></span>
<span data-ttu-id="54972-132">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="54972-132">Specifies the user password.</span></span>
<span data-ttu-id="54972-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="54972-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="54972-134">-State</span><span class="sxs-lookup"><span data-stu-id="54972-134">-State</span></span>
<span data-ttu-id="54972-135">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="54972-135">Specifies the user state.</span></span>
<span data-ttu-id="54972-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="54972-136">This parameter is optional.</span></span>
<span data-ttu-id="54972-137">Значение по умолчанию — активна.</span><span class="sxs-lookup"><span data-stu-id="54972-137">The default value is Active.</span></span>

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

### <span data-ttu-id="54972-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="54972-138">-UserId</span></span>
<span data-ttu-id="54972-139">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="54972-139">Specifies the user ID.</span></span>
<span data-ttu-id="54972-140">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="54972-140">This parameter is required.</span></span>

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

### <span data-ttu-id="54972-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54972-141">-Confirm</span></span>
<span data-ttu-id="54972-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54972-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54972-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54972-143">-WhatIf</span></span>
<span data-ttu-id="54972-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54972-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54972-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54972-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54972-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54972-146">CommonParameters</span></span>
<span data-ttu-id="54972-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54972-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54972-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54972-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54972-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54972-149">INPUTS</span></span>

### <span data-ttu-id="54972-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="54972-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="54972-151">System. String</span><span class="sxs-lookup"><span data-stu-id="54972-151">System.String</span></span>

### <span data-ttu-id="54972-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="54972-152">System.Security.SecureString</span></span>

### <span data-ttu-id="54972-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="54972-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="54972-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54972-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="54972-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54972-155">OUTPUTS</span></span>

### <span data-ttu-id="54972-156">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54972-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="54972-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="54972-157">NOTES</span></span>

## <span data-ttu-id="54972-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54972-158">RELATED LINKS</span></span>

[<span data-ttu-id="54972-159">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54972-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="54972-160">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54972-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="54972-161">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54972-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


