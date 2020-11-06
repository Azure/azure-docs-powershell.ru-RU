---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ee1ac7cda19f2b37ac1313d30075aa9c620bbd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568267"
---
# <span data-ttu-id="3d61c-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d61c-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3d61c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d61c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d61c-103">Удаление поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="3d61c-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d61c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d61c-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d61c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d61c-105">DESCRIPTION</span></span>
<span data-ttu-id="3d61c-106">Командлет **Remove-AzureRmApiManagementOpenIdConnectProvider** удаляет поставщик соединения OpenID для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="3d61c-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="3d61c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d61c-107">EXAMPLES</span></span>

### <span data-ttu-id="3d61c-108">Пример 1: Удаление поставщика</span><span class="sxs-lookup"><span data-stu-id="3d61c-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="3d61c-109">Эта команда удаляет поставщика с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="3d61c-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="3d61c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d61c-110">PARAMETERS</span></span>

### <span data-ttu-id="3d61c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3d61c-111">-Context</span></span>
<span data-ttu-id="3d61c-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3d61c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3d61c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d61c-113">-DefaultProfile</span></span>
<span data-ttu-id="3d61c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d61c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3d61c-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="3d61c-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="3d61c-116">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d61c-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3d61c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d61c-117">-PassThru</span></span>
<span data-ttu-id="3d61c-118">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3d61c-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="3d61c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d61c-119">-Confirm</span></span>
<span data-ttu-id="3d61c-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d61c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d61c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d61c-121">-WhatIf</span></span>
<span data-ttu-id="3d61c-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d61c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d61c-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d61c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d61c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d61c-124">CommonParameters</span></span>
<span data-ttu-id="3d61c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d61c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d61c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d61c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d61c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d61c-127">INPUTS</span></span>

### <span data-ttu-id="3d61c-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="3d61c-128">None</span></span>
<span data-ttu-id="3d61c-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3d61c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d61c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d61c-130">OUTPUTS</span></span>

### <span data-ttu-id="3d61c-131">Значением</span><span class="sxs-lookup"><span data-stu-id="3d61c-131">Boolean</span></span>

## <span data-ttu-id="3d61c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d61c-132">NOTES</span></span>

## <span data-ttu-id="3d61c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d61c-133">RELATED LINKS</span></span>

[<span data-ttu-id="3d61c-134">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d61c-134">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3d61c-135">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d61c-135">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3d61c-136">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3d61c-136">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


