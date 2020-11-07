---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 5258b041f2858ce766f5b6e932412986545ccf13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901661"
---
# <span data-ttu-id="2f746-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2f746-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2f746-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f746-102">SYNOPSIS</span></span>
<span data-ttu-id="2f746-103">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2f746-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="2f746-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f746-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f746-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f746-105">DESCRIPTION</span></span>
<span data-ttu-id="2f746-106">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2f746-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="2f746-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f746-107">EXAMPLES</span></span>

### <span data-ttu-id="2f746-108">Удаляет параметры поставщика удостоверений Facebook из службы ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2f746-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="2f746-109">Удаление конфигурации, связанной с конфигурацией поставщика удостоверений Facebook.</span><span class="sxs-lookup"><span data-stu-id="2f746-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="2f746-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f746-110">PARAMETERS</span></span>

### <span data-ttu-id="2f746-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2f746-111">-Context</span></span>
<span data-ttu-id="2f746-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2f746-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2f746-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2f746-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2f746-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f746-114">-DefaultProfile</span></span>
<span data-ttu-id="2f746-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f746-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f746-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f746-116">-PassThru</span></span>
<span data-ttu-id="2f746-117">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2f746-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="2f746-118">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="2f746-118">-Type</span></span>
<span data-ttu-id="2f746-119">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2f746-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="2f746-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2f746-120">This parameter is required.</span></span>

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

### <span data-ttu-id="2f746-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f746-121">-Confirm</span></span>
<span data-ttu-id="2f746-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f746-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f746-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f746-123">-WhatIf</span></span>
<span data-ttu-id="2f746-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f746-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f746-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f746-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f746-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f746-126">CommonParameters</span></span>
<span data-ttu-id="2f746-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f746-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f746-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f746-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f746-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f746-129">INPUTS</span></span>

### <span data-ttu-id="2f746-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2f746-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f746-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="2f746-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="2f746-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2f746-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f746-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f746-133">OUTPUTS</span></span>

### <span data-ttu-id="2f746-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f746-134">System.Boolean</span></span>

## <span data-ttu-id="2f746-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f746-135">NOTES</span></span>

## <span data-ttu-id="2f746-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f746-136">RELATED LINKS</span></span>

[<span data-ttu-id="2f746-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2f746-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="2f746-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2f746-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="2f746-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2f746-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

