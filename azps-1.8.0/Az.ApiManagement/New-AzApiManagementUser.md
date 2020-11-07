---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 30ff5f7d9ead2226c6c03b4707af9c20ff40d405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901709"
---
# <span data-ttu-id="1d9c2-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1d9c2-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="1d9c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9c2-103">Регистрация нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-103">Registers a new user.</span></span>

## <span data-ttu-id="1d9c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d9c2-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d9c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d9c2-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9c2-106">Командлет **New-AzApiManagementUser** регистрирует нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="1d9c2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d9c2-107">EXAMPLES</span></span>

### <span data-ttu-id="1d9c2-108">Пример 1: регистрация нового пользователя</span><span class="sxs-lookup"><span data-stu-id="1d9c2-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="1d9c2-109">Эта команда регистрирует нового пользователя с именем Patti Белова.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="1d9c2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d9c2-110">PARAMETERS</span></span>

### <span data-ttu-id="1d9c2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1d9c2-111">-Context</span></span>
<span data-ttu-id="1d9c2-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1d9c2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1d9c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9c2-113">-DefaultProfile</span></span>
<span data-ttu-id="1d9c2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d9c2-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="1d9c2-115">-Email</span></span>
<span data-ttu-id="1d9c2-116">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="1d9c2-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="1d9c2-117">-FirstName</span></span>
<span data-ttu-id="1d9c2-118">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="1d9c2-119">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1d9c2-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="1d9c2-120">-LastName</span></span>
<span data-ttu-id="1d9c2-121">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="1d9c2-122">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1d9c2-123">-Примечание</span><span class="sxs-lookup"><span data-stu-id="1d9c2-123">-Note</span></span>
<span data-ttu-id="1d9c2-124">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-124">Specifies a note about the user.</span></span>
<span data-ttu-id="1d9c2-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-125">This parameter is optional.</span></span>
<span data-ttu-id="1d9c2-126">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="1d9c2-127">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="1d9c2-127">-Password</span></span>
<span data-ttu-id="1d9c2-128">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-128">Specifies the user password.</span></span>
<span data-ttu-id="1d9c2-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-129">This parameter is required.</span></span>

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

### <span data-ttu-id="1d9c2-130">-State</span><span class="sxs-lookup"><span data-stu-id="1d9c2-130">-State</span></span>
<span data-ttu-id="1d9c2-131">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-131">Specifies the user state.</span></span>
<span data-ttu-id="1d9c2-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-132">This parameter is optional.</span></span>
<span data-ttu-id="1d9c2-133">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="1d9c2-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="1d9c2-134">-UserId</span></span>
<span data-ttu-id="1d9c2-135">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-135">Specifies the user ID.</span></span>
<span data-ttu-id="1d9c2-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-136">This parameter is optional.</span></span>
<span data-ttu-id="1d9c2-137">Если этот параметр не указан, этот командлет создает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="1d9c2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9c2-138">CommonParameters</span></span>
<span data-ttu-id="1d9c2-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d9c2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9c2-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d9c2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9c2-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d9c2-141">INPUTS</span></span>

### <span data-ttu-id="1d9c2-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1d9c2-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1d9c2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1d9c2-143">System.String</span></span>

### <span data-ttu-id="1d9c2-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1d9c2-144">System.Security.SecureString</span></span>

### <span data-ttu-id="1d9c2-145">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementUserState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="1d9c2-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1d9c2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d9c2-146">OUTPUTS</span></span>

### <span data-ttu-id="1d9c2-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1d9c2-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="1d9c2-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d9c2-148">NOTES</span></span>

## <span data-ttu-id="1d9c2-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d9c2-149">RELATED LINKS</span></span>

[<span data-ttu-id="1d9c2-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1d9c2-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="1d9c2-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1d9c2-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


