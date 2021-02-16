---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244392"
---
# <span data-ttu-id="6928e-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6928e-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="6928e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6928e-102">SYNOPSIS</span></span>
<span data-ttu-id="6928e-103">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="6928e-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="6928e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6928e-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6928e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6928e-105">DESCRIPTION</span></span>
<span data-ttu-id="6928e-106">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="6928e-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="6928e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6928e-107">EXAMPLES</span></span>

### <span data-ttu-id="6928e-108">Пример 1. Удаление параметров поставщика удостоверений Facebook из службы ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6928e-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="6928e-109">Удаляет конфигурацию, связанную с конфигурацией поставщика удостоверений Facebook.</span><span class="sxs-lookup"><span data-stu-id="6928e-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="6928e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6928e-110">PARAMETERS</span></span>

### <span data-ttu-id="6928e-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6928e-111">-Context</span></span>
<span data-ttu-id="6928e-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6928e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6928e-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6928e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6928e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6928e-114">-DefaultProfile</span></span>
<span data-ttu-id="6928e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6928e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6928e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6928e-116">-PassThru</span></span>
<span data-ttu-id="6928e-117">Указывает на то, что этот $True возвращает значение $True успешно или $False противном случае.</span><span class="sxs-lookup"><span data-stu-id="6928e-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="6928e-118">-Type</span><span class="sxs-lookup"><span data-stu-id="6928e-118">-Type</span></span>
<span data-ttu-id="6928e-119">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="6928e-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="6928e-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6928e-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6928e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6928e-121">-Confirm</span></span>
<span data-ttu-id="6928e-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6928e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6928e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6928e-123">-WhatIf</span></span>
<span data-ttu-id="6928e-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6928e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6928e-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6928e-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6928e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6928e-126">CommonParameters</span></span>
<span data-ttu-id="6928e-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6928e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6928e-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6928e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6928e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6928e-129">INPUTS</span></span>

### <span data-ttu-id="6928e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6928e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6928e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="6928e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="6928e-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6928e-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6928e-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6928e-133">OUTPUTS</span></span>

### <span data-ttu-id="6928e-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6928e-134">System.Boolean</span></span>

## <span data-ttu-id="6928e-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6928e-135">NOTES</span></span>

## <span data-ttu-id="6928e-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6928e-136">RELATED LINKS</span></span>

[<span data-ttu-id="6928e-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6928e-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="6928e-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6928e-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="6928e-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6928e-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

