---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423535"
---
# <span data-ttu-id="74f29-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74f29-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="74f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f29-102">SYNOPSIS</span></span>
<span data-ttu-id="74f29-103">Регистрация нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f29-103">Registers a new user.</span></span>

## <span data-ttu-id="74f29-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="74f29-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f29-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74f29-105">DESCRIPTION</span></span>
<span data-ttu-id="74f29-106">Новый **пользователь регистрируется стебом New-AzApiManagementUser.**</span><span class="sxs-lookup"><span data-stu-id="74f29-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="74f29-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="74f29-107">EXAMPLES</span></span>

### <span data-ttu-id="74f29-108">Пример 1. Регистрация нового пользователя</span><span class="sxs-lookup"><span data-stu-id="74f29-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="74f29-109">Эта команда регистрирует нового пользователя с именем Николай Полномер.</span><span class="sxs-lookup"><span data-stu-id="74f29-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="74f29-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74f29-110">PARAMETERS</span></span>

### <span data-ttu-id="74f29-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="74f29-111">-Context</span></span>
<span data-ttu-id="74f29-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="74f29-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="74f29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f29-113">-DefaultProfile</span></span>
<span data-ttu-id="74f29-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74f29-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f29-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="74f29-115">-Email</span></span>
<span data-ttu-id="74f29-116">Определяет адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f29-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="74f29-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="74f29-117">-FirstName</span></span>
<span data-ttu-id="74f29-118">Указывает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f29-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="74f29-119">Этот параметр должен иметь длину от 1 до 100 знаков.</span><span class="sxs-lookup"><span data-stu-id="74f29-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="74f29-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="74f29-120">-LastName</span></span>
<span data-ttu-id="74f29-121">Указывает фамилию пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f29-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="74f29-122">Этот параметр должен иметь длину от 1 до 100 знаков.</span><span class="sxs-lookup"><span data-stu-id="74f29-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="74f29-123">-Note</span><span class="sxs-lookup"><span data-stu-id="74f29-123">-Note</span></span>
<span data-ttu-id="74f29-124">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="74f29-124">Specifies a note about the user.</span></span>
<span data-ttu-id="74f29-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="74f29-125">This parameter is optional.</span></span>
<span data-ttu-id="74f29-126">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="74f29-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="74f29-127">-Password</span><span class="sxs-lookup"><span data-stu-id="74f29-127">-Password</span></span>
<span data-ttu-id="74f29-128">Определяет пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f29-128">Specifies the user password.</span></span>
<span data-ttu-id="74f29-129">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="74f29-129">This parameter is required.</span></span>

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

### <span data-ttu-id="74f29-130">-State</span><span class="sxs-lookup"><span data-stu-id="74f29-130">-State</span></span>
<span data-ttu-id="74f29-131">Определяет состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f29-131">Specifies the user state.</span></span>
<span data-ttu-id="74f29-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="74f29-132">This parameter is optional.</span></span>
<span data-ttu-id="74f29-133">По умолчанию этот параметр имеет значение $Null.</span><span class="sxs-lookup"><span data-stu-id="74f29-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="74f29-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="74f29-134">-UserId</span></span>
<span data-ttu-id="74f29-135">Определяет ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f29-135">Specifies the user ID.</span></span>
<span data-ttu-id="74f29-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="74f29-136">This parameter is optional.</span></span>
<span data-ttu-id="74f29-137">Если этот параметр не указан, этот cmdlet создает ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f29-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="74f29-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f29-138">CommonParameters</span></span>
<span data-ttu-id="74f29-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f29-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f29-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74f29-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f29-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74f29-141">INPUTS</span></span>

### <span data-ttu-id="74f29-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="74f29-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="74f29-143">System.String</span><span class="sxs-lookup"><span data-stu-id="74f29-143">System.String</span></span>

### <span data-ttu-id="74f29-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="74f29-144">System.Security.SecureString</span></span>

### <span data-ttu-id="74f29-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="74f29-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="74f29-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74f29-146">OUTPUTS</span></span>

### <span data-ttu-id="74f29-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74f29-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="74f29-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="74f29-148">NOTES</span></span>

## <span data-ttu-id="74f29-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74f29-149">RELATED LINKS</span></span>

[<span data-ttu-id="74f29-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74f29-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="74f29-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="74f29-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


