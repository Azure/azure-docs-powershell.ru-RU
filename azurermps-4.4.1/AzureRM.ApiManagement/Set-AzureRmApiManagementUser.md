---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557975"
---
# <span data-ttu-id="02010-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="02010-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="02010-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02010-102">SYNOPSIS</span></span>
<span data-ttu-id="02010-103">Настройка сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="02010-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02010-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02010-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02010-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02010-105">DESCRIPTION</span></span>
<span data-ttu-id="02010-106">Командлет **Set-AzureRmApiManagementUser** задает сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="02010-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="02010-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02010-107">EXAMPLES</span></span>

### <span data-ttu-id="02010-108">Пример 1: изменение пароля пользователя, адреса электронной почты и состояния</span><span class="sxs-lookup"><span data-stu-id="02010-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="02010-109">Эта команда задает новый пароль пользователя и адрес электронной почты, а также блокирует пользователя.</span><span class="sxs-lookup"><span data-stu-id="02010-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="02010-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02010-110">PARAMETERS</span></span>

### <span data-ttu-id="02010-111">-Context</span><span class="sxs-lookup"><span data-stu-id="02010-111">-Context</span></span>
<span data-ttu-id="02010-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="02010-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="02010-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="02010-113">This parameter is required.</span></span>

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

### <span data-ttu-id="02010-114">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="02010-114">-Email</span></span>
<span data-ttu-id="02010-115">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="02010-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="02010-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="02010-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="02010-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="02010-117">-FirstName</span></span>
<span data-ttu-id="02010-118">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="02010-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="02010-119">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="02010-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="02010-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="02010-120">-LastName</span></span>
<span data-ttu-id="02010-121">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="02010-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="02010-122">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="02010-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="02010-123">-Примечание</span><span class="sxs-lookup"><span data-stu-id="02010-123">-Note</span></span>
<span data-ttu-id="02010-124">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="02010-124">Specifies a note about the user.</span></span>
<span data-ttu-id="02010-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="02010-125">This parameter is optional.</span></span>
<span data-ttu-id="02010-126">Значение этого параметра по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="02010-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="02010-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02010-127">-PassThru</span></span>
<span data-ttu-id="02010-128">PassThru</span><span class="sxs-lookup"><span data-stu-id="02010-128">passthru</span></span>

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

### <span data-ttu-id="02010-129">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="02010-129">-Password</span></span>
<span data-ttu-id="02010-130">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="02010-130">Specifies the user password.</span></span>
<span data-ttu-id="02010-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="02010-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="02010-132">-State</span><span class="sxs-lookup"><span data-stu-id="02010-132">-State</span></span>
<span data-ttu-id="02010-133">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="02010-133">Specifies the user state.</span></span>
<span data-ttu-id="02010-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="02010-134">This parameter is optional.</span></span>
<span data-ttu-id="02010-135">Значение по умолчанию — активна.</span><span class="sxs-lookup"><span data-stu-id="02010-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02010-136">-UserId</span><span class="sxs-lookup"><span data-stu-id="02010-136">-UserId</span></span>
<span data-ttu-id="02010-137">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="02010-137">Specifies the user ID.</span></span>
<span data-ttu-id="02010-138">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="02010-138">This parameter is required.</span></span>

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

### <span data-ttu-id="02010-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02010-139">-DefaultProfile</span></span>
<span data-ttu-id="02010-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02010-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02010-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02010-141">CommonParameters</span></span>
<span data-ttu-id="02010-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02010-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02010-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02010-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02010-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02010-144">INPUTS</span></span>

## <span data-ttu-id="02010-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02010-145">OUTPUTS</span></span>

### <span data-ttu-id="02010-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="02010-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="02010-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="02010-147">NOTES</span></span>

## <span data-ttu-id="02010-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02010-148">RELATED LINKS</span></span>

[<span data-ttu-id="02010-149">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="02010-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="02010-150">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="02010-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="02010-151">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="02010-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


