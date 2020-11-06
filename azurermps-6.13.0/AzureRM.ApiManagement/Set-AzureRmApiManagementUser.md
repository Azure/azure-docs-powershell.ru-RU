---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: 705deeb8e9b248b480bd2a28662cc7e968f8c228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558596"
---
# <span data-ttu-id="c2176-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c2176-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="c2176-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2176-102">SYNOPSIS</span></span>
<span data-ttu-id="c2176-103">Настройка сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="c2176-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2176-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2176-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2176-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2176-105">DESCRIPTION</span></span>
<span data-ttu-id="c2176-106">Командлет **Set-AzureRmApiManagementUser** задает сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="c2176-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="c2176-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2176-107">EXAMPLES</span></span>

### <span data-ttu-id="c2176-108">Пример 1: изменение пароля пользователя, адреса электронной почты и состояния</span><span class="sxs-lookup"><span data-stu-id="c2176-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="c2176-109">Эта команда задает новый пароль пользователя и адрес электронной почты, а также блокирует пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2176-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="c2176-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2176-110">PARAMETERS</span></span>

### <span data-ttu-id="c2176-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c2176-111">-Context</span></span>
<span data-ttu-id="c2176-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c2176-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c2176-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c2176-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2176-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2176-114">-DefaultProfile</span></span>
<span data-ttu-id="c2176-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2176-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2176-116">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="c2176-116">-Email</span></span>
<span data-ttu-id="c2176-117">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2176-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="c2176-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c2176-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="c2176-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="c2176-119">-FirstName</span></span>
<span data-ttu-id="c2176-120">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2176-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="c2176-121">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="c2176-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="c2176-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="c2176-122">-LastName</span></span>
<span data-ttu-id="c2176-123">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2176-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="c2176-124">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="c2176-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="c2176-125">-Примечание</span><span class="sxs-lookup"><span data-stu-id="c2176-125">-Note</span></span>
<span data-ttu-id="c2176-126">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="c2176-126">Specifies a note about the user.</span></span>
<span data-ttu-id="c2176-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c2176-127">This parameter is optional.</span></span>
<span data-ttu-id="c2176-128">Значение этого параметра по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="c2176-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="c2176-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2176-129">-PassThru</span></span>
<span data-ttu-id="c2176-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="c2176-130">passthru</span></span>

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

### <span data-ttu-id="c2176-131">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="c2176-131">-Password</span></span>
<span data-ttu-id="c2176-132">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2176-132">Specifies the user password.</span></span>
<span data-ttu-id="c2176-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c2176-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="c2176-134">-State</span><span class="sxs-lookup"><span data-stu-id="c2176-134">-State</span></span>
<span data-ttu-id="c2176-135">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2176-135">Specifies the user state.</span></span>
<span data-ttu-id="c2176-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c2176-136">This parameter is optional.</span></span>
<span data-ttu-id="c2176-137">Значение по умолчанию — активна.</span><span class="sxs-lookup"><span data-stu-id="c2176-137">The default value is Active.</span></span>

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

### <span data-ttu-id="c2176-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="c2176-138">-UserId</span></span>
<span data-ttu-id="c2176-139">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2176-139">Specifies the user ID.</span></span>
<span data-ttu-id="c2176-140">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c2176-140">This parameter is required.</span></span>

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

### <span data-ttu-id="c2176-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2176-141">CommonParameters</span></span>
<span data-ttu-id="c2176-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2176-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2176-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2176-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2176-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2176-144">INPUTS</span></span>

### <span data-ttu-id="c2176-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c2176-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c2176-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c2176-146">System.String</span></span>

### <span data-ttu-id="c2176-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c2176-147">System.Security.SecureString</span></span>

### <span data-ttu-id="c2176-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="c2176-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="c2176-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2176-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c2176-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2176-150">OUTPUTS</span></span>

### <span data-ttu-id="c2176-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c2176-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="c2176-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2176-152">NOTES</span></span>

## <span data-ttu-id="c2176-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2176-153">RELATED LINKS</span></span>

[<span data-ttu-id="c2176-154">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c2176-154">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="c2176-155">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c2176-155">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="c2176-156">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c2176-156">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


