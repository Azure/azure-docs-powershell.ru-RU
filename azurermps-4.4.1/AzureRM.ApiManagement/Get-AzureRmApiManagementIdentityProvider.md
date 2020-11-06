---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565760"
---
# <span data-ttu-id="94cf8-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="94cf8-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="94cf8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="94cf8-103">Получение сведений о конфигурации поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="94cf8-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94cf8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94cf8-104">SYNTAX</span></span>

### <span data-ttu-id="94cf8-105">AllIdentityProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94cf8-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94cf8-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="94cf8-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94cf8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94cf8-107">DESCRIPTION</span></span>
<span data-ttu-id="94cf8-108">Получение сведений о конфигурации поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="94cf8-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="94cf8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94cf8-109">EXAMPLES</span></span>

### <span data-ttu-id="94cf8-110">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="94cf8-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="94cf8-111">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="94cf8-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="94cf8-112">Получение всех конфигураций поставщика удостоверений в службе.</span><span class="sxs-lookup"><span data-stu-id="94cf8-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="94cf8-113">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="94cf8-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="94cf8-114">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="94cf8-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="94cf8-115">Возвращает конфигурацию поставщика удостоверений Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94cf8-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="94cf8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94cf8-116">PARAMETERS</span></span>

### <span data-ttu-id="94cf8-117">-Context</span><span class="sxs-lookup"><span data-stu-id="94cf8-117">-Context</span></span>
<span data-ttu-id="94cf8-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="94cf8-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="94cf8-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="94cf8-119">This parameter is required.</span></span>

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

### <span data-ttu-id="94cf8-120">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="94cf8-120">-Type</span></span>
<span data-ttu-id="94cf8-121">Идентификатор поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="94cf8-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="94cf8-122">Если задано значение, это попытается найти конфигурацию поставщика удостоверений с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="94cf8-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="94cf8-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="94cf8-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94cf8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94cf8-124">-DefaultProfile</span></span>
<span data-ttu-id="94cf8-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94cf8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94cf8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94cf8-126">CommonParameters</span></span>
<span data-ttu-id="94cf8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94cf8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94cf8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94cf8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94cf8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94cf8-129">INPUTS</span></span>

## <span data-ttu-id="94cf8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94cf8-130">OUTPUTS</span></span>

### <span data-ttu-id="94cf8-131">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="94cf8-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="94cf8-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="94cf8-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="94cf8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="94cf8-133">NOTES</span></span>

## <span data-ttu-id="94cf8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94cf8-134">RELATED LINKS</span></span>

