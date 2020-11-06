---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 686b988ef5bf62e5eed7e4f8fae94f6b29b1b4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560572"
---
# <span data-ttu-id="eb35d-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb35d-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="eb35d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb35d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb35d-103">Удаление поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="eb35d-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb35d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb35d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb35d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb35d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb35d-106">Командлет **Remove-AzureRmApiManagementOpenIdConnectProvider** удаляет поставщик соединения OpenID для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="eb35d-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="eb35d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb35d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb35d-108">Пример 1: Удаление поставщика</span><span class="sxs-lookup"><span data-stu-id="eb35d-108">Example 1: Remove a provider</span></span>
```
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="eb35d-109">Эта команда удаляет поставщика с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="eb35d-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="eb35d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb35d-110">PARAMETERS</span></span>

### <span data-ttu-id="eb35d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="eb35d-111">-Context</span></span>
<span data-ttu-id="eb35d-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="eb35d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eb35d-113">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="eb35d-113">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="eb35d-114">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eb35d-114">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="eb35d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb35d-115">-PassThru</span></span>
<span data-ttu-id="eb35d-116">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="eb35d-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="eb35d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb35d-117">-Confirm</span></span>
<span data-ttu-id="eb35d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb35d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb35d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb35d-119">-WhatIf</span></span>
<span data-ttu-id="eb35d-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb35d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb35d-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb35d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb35d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb35d-122">-DefaultProfile</span></span>
<span data-ttu-id="eb35d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb35d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb35d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb35d-124">CommonParameters</span></span>
<span data-ttu-id="eb35d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb35d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb35d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb35d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb35d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb35d-127">INPUTS</span></span>

## <span data-ttu-id="eb35d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb35d-128">OUTPUTS</span></span>

### <span data-ttu-id="eb35d-129">Значением</span><span class="sxs-lookup"><span data-stu-id="eb35d-129">Boolean</span></span>

## <span data-ttu-id="eb35d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb35d-130">NOTES</span></span>

## <span data-ttu-id="eb35d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb35d-131">RELATED LINKS</span></span>

[<span data-ttu-id="eb35d-132">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb35d-132">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="eb35d-133">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb35d-133">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="eb35d-134">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="eb35d-134">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


