---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 7e141cb5c1bde59bec9e981ffd228dba6db33089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959176"
---
# <span data-ttu-id="d63c5-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d63c5-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="d63c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d63c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d63c5-103">Регистрация нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="d63c5-103">Registers a new user.</span></span>

## <span data-ttu-id="d63c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d63c5-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d63c5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d63c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d63c5-106">Новый пользователь регистрируется стебом **New-AzApiManagementUser.**</span><span class="sxs-lookup"><span data-stu-id="d63c5-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="d63c5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d63c5-107">EXAMPLES</span></span>

### <span data-ttu-id="d63c5-108">Пример 1. Регистрация нового пользователя</span><span class="sxs-lookup"><span data-stu-id="d63c5-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="d63c5-109">Эта команда регистрирует нового пользователя с именем Николай Полномер.</span><span class="sxs-lookup"><span data-stu-id="d63c5-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="d63c5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d63c5-110">PARAMETERS</span></span>

### <span data-ttu-id="d63c5-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="d63c5-111">-Context</span></span>
<span data-ttu-id="d63c5-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="d63c5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d63c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d63c5-113">-DefaultProfile</span></span>
<span data-ttu-id="d63c5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d63c5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d63c5-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="d63c5-115">-Email</span></span>
<span data-ttu-id="d63c5-116">Определяет адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="d63c5-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="d63c5-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="d63c5-117">-FirstName</span></span>
<span data-ttu-id="d63c5-118">Указывает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="d63c5-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="d63c5-119">Этот параметр должен иметь длину от 1 до 100 знаков.</span><span class="sxs-lookup"><span data-stu-id="d63c5-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="d63c5-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="d63c5-120">-LastName</span></span>
<span data-ttu-id="d63c5-121">Указывает фамилию пользователя.</span><span class="sxs-lookup"><span data-stu-id="d63c5-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="d63c5-122">Этот параметр должен иметь длину от 1 до 100 знаков.</span><span class="sxs-lookup"><span data-stu-id="d63c5-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="d63c5-123">-Note</span><span class="sxs-lookup"><span data-stu-id="d63c5-123">-Note</span></span>
<span data-ttu-id="d63c5-124">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="d63c5-124">Specifies a note about the user.</span></span>
<span data-ttu-id="d63c5-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d63c5-125">This parameter is optional.</span></span>
<span data-ttu-id="d63c5-126">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="d63c5-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="d63c5-127">-Password</span><span class="sxs-lookup"><span data-stu-id="d63c5-127">-Password</span></span>
<span data-ttu-id="d63c5-128">Определяет пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="d63c5-128">Specifies the user password.</span></span>
<span data-ttu-id="d63c5-129">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d63c5-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d63c5-130">-State</span><span class="sxs-lookup"><span data-stu-id="d63c5-130">-State</span></span>
<span data-ttu-id="d63c5-131">Определяет состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="d63c5-131">Specifies the user state.</span></span>
<span data-ttu-id="d63c5-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d63c5-132">This parameter is optional.</span></span>
<span data-ttu-id="d63c5-133">По умолчанию этот параметр имеет значение $Null.</span><span class="sxs-lookup"><span data-stu-id="d63c5-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d63c5-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="d63c5-134">-UserId</span></span>
<span data-ttu-id="d63c5-135">Определяет ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="d63c5-135">Specifies the user ID.</span></span>
<span data-ttu-id="d63c5-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d63c5-136">This parameter is optional.</span></span>
<span data-ttu-id="d63c5-137">Если этот параметр не указан, этот cmdlet создает ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="d63c5-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="d63c5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d63c5-138">CommonParameters</span></span>
<span data-ttu-id="d63c5-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d63c5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d63c5-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d63c5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d63c5-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d63c5-141">INPUTS</span></span>

### <span data-ttu-id="d63c5-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d63c5-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d63c5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d63c5-143">System.String</span></span>

### <span data-ttu-id="d63c5-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d63c5-144">System.Security.SecureString</span></span>

### <span data-ttu-id="d63c5-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d63c5-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d63c5-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d63c5-146">OUTPUTS</span></span>

### <span data-ttu-id="d63c5-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d63c5-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="d63c5-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d63c5-148">NOTES</span></span>

## <span data-ttu-id="d63c5-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d63c5-149">RELATED LINKS</span></span>

[<span data-ttu-id="d63c5-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d63c5-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="d63c5-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d63c5-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


