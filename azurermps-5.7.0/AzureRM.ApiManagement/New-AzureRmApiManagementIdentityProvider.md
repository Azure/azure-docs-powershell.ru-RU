---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 470692c946175c75bf21bd613e6bbf3590854768
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732551"
---
# <span data-ttu-id="77eca-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="77eca-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="77eca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77eca-102">SYNOPSIS</span></span>
<span data-ttu-id="77eca-103">Создает новую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="77eca-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77eca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77eca-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77eca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77eca-105">DESCRIPTION</span></span>
<span data-ttu-id="77eca-106">Создает новую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="77eca-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="77eca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77eca-107">EXAMPLES</span></span>

### <span data-ttu-id="77eca-108">Пример 1: Настройка Facebook в качестве поставщика удостоверений для входа на портал разработчика</span><span class="sxs-lookup"><span data-stu-id="77eca-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="77eca-109">Эта команда настраивает удостоверение Facebook как одобренного поставщика удостоверений на портале разработчика службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="77eca-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="77eca-110">Это берет на себя в качестве входных данных ClientId и ClientSecret приложения Facebook.</span><span class="sxs-lookup"><span data-stu-id="77eca-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="77eca-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77eca-111">PARAMETERS</span></span>

### <span data-ttu-id="77eca-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="77eca-112">-AllowedTenants</span></span>
<span data-ttu-id="77eca-113">Список разрешенных клиентов Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="77eca-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77eca-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="77eca-114">-ClientId</span></span>
<span data-ttu-id="77eca-115">Идентификатор клиента приложения в поставщике внешней идентификации.</span><span class="sxs-lookup"><span data-stu-id="77eca-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="77eca-116">Это идентификатор приложения для входа в Facebook, идентификатор клиента для входа в Google, идентификатор приложения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77eca-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="77eca-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="77eca-117">-ClientSecret</span></span>
<span data-ttu-id="77eca-118">Секретный ключ клиента приложения во внешнем поставщике удостоверений, используемый для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="77eca-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="77eca-119">Например, это конфиденциальное приложение для входа в Facebook, ключ API для входа в Google, Открытый ключ для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77eca-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="77eca-120">-Context</span><span class="sxs-lookup"><span data-stu-id="77eca-120">-Context</span></span>
<span data-ttu-id="77eca-121">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="77eca-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="77eca-122">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="77eca-122">This parameter is required.</span></span>

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

### <span data-ttu-id="77eca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77eca-123">-DefaultProfile</span></span>
<span data-ttu-id="77eca-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77eca-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="77eca-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="77eca-125">-Type</span></span>
<span data-ttu-id="77eca-126">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="77eca-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="77eca-127">Если задано значение, это попытается найти конфигурацию поставщика удостоверений с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="77eca-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="77eca-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="77eca-128">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77eca-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77eca-129">-Confirm</span></span>
<span data-ttu-id="77eca-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77eca-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77eca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77eca-131">-WhatIf</span></span>
<span data-ttu-id="77eca-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77eca-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77eca-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77eca-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77eca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77eca-134">CommonParameters</span></span>
<span data-ttu-id="77eca-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77eca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77eca-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77eca-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77eca-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77eca-137">INPUTS</span></span>

### <span data-ttu-id="77eca-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="77eca-138">None</span></span>
<span data-ttu-id="77eca-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="77eca-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77eca-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77eca-140">OUTPUTS</span></span>

### <span data-ttu-id="77eca-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="77eca-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="77eca-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="77eca-142">NOTES</span></span>

## <span data-ttu-id="77eca-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77eca-143">RELATED LINKS</span></span>

[<span data-ttu-id="77eca-144">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="77eca-144">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="77eca-145">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="77eca-145">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="77eca-146">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="77eca-146">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
