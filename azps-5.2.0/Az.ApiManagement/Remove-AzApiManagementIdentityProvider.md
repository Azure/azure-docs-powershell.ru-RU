---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411559"
---
# <span data-ttu-id="2c245-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2c245-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2c245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c245-102">SYNOPSIS</span></span>
<span data-ttu-id="2c245-103">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2c245-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="2c245-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c245-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c245-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c245-105">DESCRIPTION</span></span>
<span data-ttu-id="2c245-106">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2c245-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="2c245-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c245-107">EXAMPLES</span></span>

### <span data-ttu-id="2c245-108">Пример 1. Удаление параметров поставщика удостоверений Facebook из службы ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c245-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="2c245-109">Удаляет конфигурацию, связанную с конфигурацией поставщика удостоверений Facebook.</span><span class="sxs-lookup"><span data-stu-id="2c245-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="2c245-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c245-110">PARAMETERS</span></span>

### <span data-ttu-id="2c245-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="2c245-111">-Context</span></span>
<span data-ttu-id="2c245-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2c245-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2c245-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="2c245-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2c245-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c245-114">-DefaultProfile</span></span>
<span data-ttu-id="2c245-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c245-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c245-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c245-116">-PassThru</span></span>
<span data-ttu-id="2c245-117">Указывает на то, что этот $True возвращает значение $True успешно или $False противном случае.</span><span class="sxs-lookup"><span data-stu-id="2c245-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="2c245-118">-Type</span><span class="sxs-lookup"><span data-stu-id="2c245-118">-Type</span></span>
<span data-ttu-id="2c245-119">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2c245-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="2c245-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="2c245-120">This parameter is required.</span></span>

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

### <span data-ttu-id="2c245-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c245-121">-Confirm</span></span>
<span data-ttu-id="2c245-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c245-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c245-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c245-123">-WhatIf</span></span>
<span data-ttu-id="2c245-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c245-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c245-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2c245-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c245-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c245-126">CommonParameters</span></span>
<span data-ttu-id="2c245-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c245-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c245-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c245-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c245-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c245-129">INPUTS</span></span>

### <span data-ttu-id="2c245-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2c245-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2c245-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="2c245-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="2c245-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2c245-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2c245-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c245-133">OUTPUTS</span></span>

### <span data-ttu-id="2c245-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c245-134">System.Boolean</span></span>

## <span data-ttu-id="2c245-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c245-135">NOTES</span></span>

## <span data-ttu-id="2c245-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c245-136">RELATED LINKS</span></span>

[<span data-ttu-id="2c245-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2c245-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="2c245-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2c245-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="2c245-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2c245-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

