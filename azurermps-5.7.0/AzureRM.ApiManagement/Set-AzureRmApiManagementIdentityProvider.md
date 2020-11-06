---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e45ec5a3d49bf82ab945a3ef3b41362a1e1e2bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569080"
---
# <span data-ttu-id="07e59-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="07e59-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="07e59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07e59-102">SYNOPSIS</span></span>
<span data-ttu-id="07e59-103">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="07e59-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07e59-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07e59-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07e59-105">DESCRIPTION</span></span>
<span data-ttu-id="07e59-106">Обновляет конфигурацию существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="07e59-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="07e59-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07e59-107">EXAMPLES</span></span>

### <span data-ttu-id="07e59-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07e59-108">Example 1</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="07e59-109">Командлет обновляет секретный ключ клиента поставщика удостоверений Facebook;</span><span class="sxs-lookup"><span data-stu-id="07e59-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="07e59-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07e59-110">PARAMETERS</span></span>

### <span data-ttu-id="07e59-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="07e59-111">-AllowedTenants</span></span>
<span data-ttu-id="07e59-112">Список разрешенных клиентов Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07e59-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="07e59-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="07e59-113">-ClientId</span></span>
<span data-ttu-id="07e59-114">Идентификатор клиента приложения в поставщике внешней идентификации.</span><span class="sxs-lookup"><span data-stu-id="07e59-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="07e59-115">Это идентификатор приложения для входа в Facebook, идентификатор клиента для входа в Google, идентификатор приложения для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="07e59-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="07e59-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="07e59-116">-ClientSecret</span></span>
<span data-ttu-id="07e59-117">Секретный ключ клиента приложения во внешнем поставщике удостоверений, используемый для проверки подлинности запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="07e59-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="07e59-118">Например, это конфиденциальное приложение для входа в Facebook, ключ API для входа в Google, Открытый ключ для Microsoft.</span><span class="sxs-lookup"><span data-stu-id="07e59-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="07e59-119">-Context</span><span class="sxs-lookup"><span data-stu-id="07e59-119">-Context</span></span>
<span data-ttu-id="07e59-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="07e59-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="07e59-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="07e59-121">This parameter is required.</span></span>

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

### <span data-ttu-id="07e59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e59-122">-DefaultProfile</span></span>
<span data-ttu-id="07e59-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07e59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="07e59-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07e59-124">-PassThru</span></span>
<span data-ttu-id="07e59-125">Указывает на то, что этот командлет возвращает  **PsApiManagementIdentityProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="07e59-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


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

### <span data-ttu-id="07e59-126">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="07e59-126">-Type</span></span>
<span data-ttu-id="07e59-127">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="07e59-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="07e59-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="07e59-128">This parameter is required.</span></span>

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

### <span data-ttu-id="07e59-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07e59-129">-Confirm</span></span>
<span data-ttu-id="07e59-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="07e59-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07e59-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07e59-131">-WhatIf</span></span>
<span data-ttu-id="07e59-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="07e59-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07e59-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="07e59-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07e59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e59-134">CommonParameters</span></span>
<span data-ttu-id="07e59-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07e59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e59-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e59-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e59-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07e59-137">INPUTS</span></span>

### <span data-ttu-id="07e59-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="07e59-138">None</span></span>
<span data-ttu-id="07e59-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="07e59-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07e59-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07e59-140">OUTPUTS</span></span>

### <span data-ttu-id="07e59-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="07e59-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="07e59-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="07e59-142">NOTES</span></span>

## <span data-ttu-id="07e59-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07e59-143">RELATED LINKS</span></span>

[<span data-ttu-id="07e59-144">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="07e59-144">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="07e59-145">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="07e59-145">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="07e59-146">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="07e59-146">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
