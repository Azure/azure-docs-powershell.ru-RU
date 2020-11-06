---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6b4ccac87f963f9948c67d3162f1677b9860583b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556912"
---
# <span data-ttu-id="789c0-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="789c0-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="789c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="789c0-102">SYNOPSIS</span></span>
<span data-ttu-id="789c0-103">Удаление поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="789c0-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="789c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="789c0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="789c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="789c0-105">DESCRIPTION</span></span>
<span data-ttu-id="789c0-106">Командлет **Remove-AzureRmApiManagementOpenIdConnectProvider** удаляет поставщик соединения OpenID для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="789c0-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="789c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="789c0-107">EXAMPLES</span></span>

### <span data-ttu-id="789c0-108">Пример 1: Удаление поставщика</span><span class="sxs-lookup"><span data-stu-id="789c0-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="789c0-109">Эта команда удаляет поставщика с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="789c0-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="789c0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="789c0-110">PARAMETERS</span></span>

### <span data-ttu-id="789c0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="789c0-111">-Context</span></span>
<span data-ttu-id="789c0-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="789c0-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="789c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789c0-113">-DefaultProfile</span></span>
<span data-ttu-id="789c0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="789c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="789c0-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="789c0-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="789c0-116">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="789c0-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="789c0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="789c0-117">-PassThru</span></span>
<span data-ttu-id="789c0-118">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="789c0-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="789c0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="789c0-119">-Confirm</span></span>
<span data-ttu-id="789c0-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="789c0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789c0-121">-WhatIf</span></span>
<span data-ttu-id="789c0-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="789c0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="789c0-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="789c0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789c0-124">CommonParameters</span></span>
<span data-ttu-id="789c0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="789c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789c0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789c0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789c0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="789c0-127">INPUTS</span></span>

### <span data-ttu-id="789c0-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="789c0-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="789c0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="789c0-129">System.String</span></span>

### <span data-ttu-id="789c0-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="789c0-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="789c0-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="789c0-131">OUTPUTS</span></span>

### <span data-ttu-id="789c0-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="789c0-132">System.Boolean</span></span>

## <span data-ttu-id="789c0-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="789c0-133">NOTES</span></span>

## <span data-ttu-id="789c0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="789c0-134">RELATED LINKS</span></span>

[<span data-ttu-id="789c0-135">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="789c0-135">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="789c0-136">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="789c0-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="789c0-137">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="789c0-137">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


