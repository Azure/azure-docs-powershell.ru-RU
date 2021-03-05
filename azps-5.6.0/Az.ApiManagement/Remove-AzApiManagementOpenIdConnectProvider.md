---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3d7d6600e7e26202c920499a615f4124767c830c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988515"
---
# <span data-ttu-id="61d9a-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="61d9a-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="61d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="61d9a-103">Удаляет поставщика OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="61d9a-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="61d9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61d9a-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61d9a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="61d9a-106">Из-за выполнения команды **Remove-AzApiManagementOpenIdConnectProvider** удаляется поставщик OpenID Connect для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="61d9a-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="61d9a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="61d9a-108">Пример 1. Удаление поставщика</span><span class="sxs-lookup"><span data-stu-id="61d9a-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="61d9a-109">Эта команда удаляет поставщика, который имеет ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="61d9a-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="61d9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61d9a-110">PARAMETERS</span></span>

### <span data-ttu-id="61d9a-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="61d9a-111">-Context</span></span>
<span data-ttu-id="61d9a-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="61d9a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="61d9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d9a-113">-DefaultProfile</span></span>
<span data-ttu-id="61d9a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61d9a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61d9a-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="61d9a-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="61d9a-116">Определяет код поставщика, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61d9a-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61d9a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61d9a-117">-PassThru</span></span>
<span data-ttu-id="61d9a-118">Указывает на то, что этот $True возвращает значение $True успешно или $False противном случае.</span><span class="sxs-lookup"><span data-stu-id="61d9a-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="61d9a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61d9a-119">-Confirm</span></span>
<span data-ttu-id="61d9a-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="61d9a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61d9a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61d9a-121">-WhatIf</span></span>
<span data-ttu-id="61d9a-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61d9a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61d9a-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61d9a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61d9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d9a-124">CommonParameters</span></span>
<span data-ttu-id="61d9a-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d9a-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61d9a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d9a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61d9a-127">INPUTS</span></span>

### <span data-ttu-id="61d9a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="61d9a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="61d9a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="61d9a-129">System.String</span></span>

### <span data-ttu-id="61d9a-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61d9a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="61d9a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61d9a-131">OUTPUTS</span></span>

### <span data-ttu-id="61d9a-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61d9a-132">System.Boolean</span></span>

## <span data-ttu-id="61d9a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61d9a-133">NOTES</span></span>

## <span data-ttu-id="61d9a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61d9a-134">RELATED LINKS</span></span>

[<span data-ttu-id="61d9a-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="61d9a-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="61d9a-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="61d9a-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="61d9a-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="61d9a-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


