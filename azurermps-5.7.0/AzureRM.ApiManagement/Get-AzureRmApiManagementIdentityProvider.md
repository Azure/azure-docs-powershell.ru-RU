---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567019"
---
# <span data-ttu-id="9afa5-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9afa5-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9afa5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9afa5-102">SYNOPSIS</span></span>
<span data-ttu-id="9afa5-103">Получение сведений о конфигурации поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9afa5-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9afa5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9afa5-104">SYNTAX</span></span>

### <span data-ttu-id="9afa5-105">AllIdentityProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9afa5-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9afa5-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="9afa5-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9afa5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9afa5-107">DESCRIPTION</span></span>
<span data-ttu-id="9afa5-108">Получение сведений о конфигурации поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9afa5-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="9afa5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9afa5-109">EXAMPLES</span></span>

### <span data-ttu-id="9afa5-110">Пример 1: получение всех поставщиков удостоверений</span><span class="sxs-lookup"><span data-stu-id="9afa5-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="9afa5-111">Получение всех конфигураций поставщика удостоверений в службе.</span><span class="sxs-lookup"><span data-stu-id="9afa5-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="9afa5-112">Получение поставщика удостоверений для типа AAD</span><span class="sxs-lookup"><span data-stu-id="9afa5-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="9afa5-113">Возвращает конфигурацию поставщика удостоверений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9afa5-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="9afa5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9afa5-114">PARAMETERS</span></span>

### <span data-ttu-id="9afa5-115">-Context</span><span class="sxs-lookup"><span data-stu-id="9afa5-115">-Context</span></span>
<span data-ttu-id="9afa5-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9afa5-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9afa5-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9afa5-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9afa5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9afa5-118">-DefaultProfile</span></span>
<span data-ttu-id="9afa5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9afa5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9afa5-120">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="9afa5-120">-Type</span></span>
<span data-ttu-id="9afa5-121">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="9afa5-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="9afa5-122">Если задано значение, это попытается найти конфигурацию поставщика удостоверений с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="9afa5-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="9afa5-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9afa5-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9afa5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9afa5-124">CommonParameters</span></span>
<span data-ttu-id="9afa5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9afa5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9afa5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9afa5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9afa5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9afa5-127">INPUTS</span></span>

### <span data-ttu-id="9afa5-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="9afa5-128">None</span></span>
<span data-ttu-id="9afa5-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9afa5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9afa5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9afa5-130">OUTPUTS</span></span>

### <span data-ttu-id="9afa5-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9afa5-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="9afa5-132">Сведения о поставщике удостоверений, настроенном в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="9afa5-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="9afa5-133">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="9afa5-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="9afa5-134">Список поставщиков удостоверений, настроенных в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="9afa5-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="9afa5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9afa5-135">NOTES</span></span>

## <span data-ttu-id="9afa5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9afa5-136">RELATED LINKS</span></span>

