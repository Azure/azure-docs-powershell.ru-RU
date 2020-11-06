---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: d3825b4887d2361a4bb378bfddc3085773efd84b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568653"
---
# <span data-ttu-id="139d2-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="139d2-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="139d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="139d2-102">SYNOPSIS</span></span>
<span data-ttu-id="139d2-103">Настройка сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="139d2-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="139d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="139d2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="139d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="139d2-105">DESCRIPTION</span></span>
<span data-ttu-id="139d2-106">Командлет **Set-AzureRmApiManagementUser** задает сведения о пользователе.</span><span class="sxs-lookup"><span data-stu-id="139d2-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="139d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="139d2-107">EXAMPLES</span></span>

### <span data-ttu-id="139d2-108">Пример 1: изменение пароля пользователя, адреса электронной почты и состояния</span><span class="sxs-lookup"><span data-stu-id="139d2-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="139d2-109">Эта команда задает новый пароль пользователя и адрес электронной почты, а также блокирует пользователя.</span><span class="sxs-lookup"><span data-stu-id="139d2-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="139d2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="139d2-110">PARAMETERS</span></span>

### <span data-ttu-id="139d2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="139d2-111">-Context</span></span>
<span data-ttu-id="139d2-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="139d2-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="139d2-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="139d2-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139d2-114">-DefaultProfile</span></span>
<span data-ttu-id="139d2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="139d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-116">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="139d2-116">-Email</span></span>
<span data-ttu-id="139d2-117">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="139d2-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="139d2-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="139d2-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="139d2-119">-FirstName</span></span>
<span data-ttu-id="139d2-120">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="139d2-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="139d2-121">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="139d2-121">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="139d2-122">-LastName</span></span>
<span data-ttu-id="139d2-123">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="139d2-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="139d2-124">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="139d2-124">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-125">-Примечание</span><span class="sxs-lookup"><span data-stu-id="139d2-125">-Note</span></span>
<span data-ttu-id="139d2-126">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="139d2-126">Specifies a note about the user.</span></span>
<span data-ttu-id="139d2-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="139d2-127">This parameter is optional.</span></span>
<span data-ttu-id="139d2-128">Значение этого параметра по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="139d2-128">The default value of this parameter is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="139d2-129">-PassThru</span></span>
<span data-ttu-id="139d2-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="139d2-130">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-131">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="139d2-131">-Password</span></span>
<span data-ttu-id="139d2-132">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="139d2-132">Specifies the user password.</span></span>
<span data-ttu-id="139d2-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="139d2-133">This parameter is optional.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-134">-State</span><span class="sxs-lookup"><span data-stu-id="139d2-134">-State</span></span>
<span data-ttu-id="139d2-135">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="139d2-135">Specifies the user state.</span></span>
<span data-ttu-id="139d2-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="139d2-136">This parameter is optional.</span></span>
<span data-ttu-id="139d2-137">Значение по умолчанию — активна.</span><span class="sxs-lookup"><span data-stu-id="139d2-137">The default value is Active.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="139d2-138">-UserId</span></span>
<span data-ttu-id="139d2-139">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="139d2-139">Specifies the user ID.</span></span>
<span data-ttu-id="139d2-140">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="139d2-140">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="139d2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139d2-141">CommonParameters</span></span>
<span data-ttu-id="139d2-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="139d2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139d2-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="139d2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139d2-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="139d2-144">INPUTS</span></span>

### <span data-ttu-id="139d2-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="139d2-145">None</span></span>
<span data-ttu-id="139d2-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="139d2-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="139d2-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="139d2-147">OUTPUTS</span></span>

### <span data-ttu-id="139d2-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="139d2-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="139d2-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="139d2-149">NOTES</span></span>

## <span data-ttu-id="139d2-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="139d2-150">RELATED LINKS</span></span>

[<span data-ttu-id="139d2-151">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="139d2-151">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="139d2-152">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="139d2-152">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="139d2-153">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="139d2-153">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


