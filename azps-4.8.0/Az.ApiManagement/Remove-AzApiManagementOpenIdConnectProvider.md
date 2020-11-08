---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078539"
---
# <span data-ttu-id="3daed-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3daed-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3daed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3daed-102">SYNOPSIS</span></span>
<span data-ttu-id="3daed-103">Удаление поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="3daed-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="3daed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3daed-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3daed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3daed-105">DESCRIPTION</span></span>
<span data-ttu-id="3daed-106">Командлет **Remove-AzApiManagementOpenIdConnectProvider** удаляет поставщик соединения OpenID для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="3daed-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="3daed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3daed-107">EXAMPLES</span></span>

### <span data-ttu-id="3daed-108">Пример 1: Удаление поставщика</span><span class="sxs-lookup"><span data-stu-id="3daed-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="3daed-109">Эта команда удаляет поставщика с ИДЕНТИФИКАТОРом OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="3daed-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="3daed-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3daed-110">PARAMETERS</span></span>

### <span data-ttu-id="3daed-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3daed-111">-Context</span></span>
<span data-ttu-id="3daed-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3daed-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3daed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3daed-113">-DefaultProfile</span></span>
<span data-ttu-id="3daed-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3daed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3daed-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="3daed-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="3daed-116">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3daed-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3daed-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3daed-117">-PassThru</span></span>
<span data-ttu-id="3daed-118">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3daed-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="3daed-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3daed-119">-Confirm</span></span>
<span data-ttu-id="3daed-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3daed-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3daed-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3daed-121">-WhatIf</span></span>
<span data-ttu-id="3daed-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3daed-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3daed-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3daed-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3daed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3daed-124">CommonParameters</span></span>
<span data-ttu-id="3daed-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3daed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3daed-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3daed-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3daed-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3daed-127">INPUTS</span></span>

### <span data-ttu-id="3daed-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3daed-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3daed-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3daed-129">System.String</span></span>

### <span data-ttu-id="3daed-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3daed-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3daed-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3daed-131">OUTPUTS</span></span>

### <span data-ttu-id="3daed-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3daed-132">System.Boolean</span></span>

## <span data-ttu-id="3daed-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3daed-133">NOTES</span></span>

## <span data-ttu-id="3daed-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3daed-134">RELATED LINKS</span></span>

[<span data-ttu-id="3daed-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3daed-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3daed-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3daed-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3daed-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3daed-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


