---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556919"
---
# <span data-ttu-id="24dca-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="24dca-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="24dca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24dca-102">SYNOPSIS</span></span>
<span data-ttu-id="24dca-103">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="24dca-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24dca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24dca-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24dca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24dca-105">DESCRIPTION</span></span>
<span data-ttu-id="24dca-106">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="24dca-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="24dca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24dca-107">EXAMPLES</span></span>

### <span data-ttu-id="24dca-108">Удаляет параметры поставщика удостоверений Facebook из службы ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24dca-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="24dca-109">Удаление конфигурации, связанной с конфигурацией поставщика удостоверений Facebook.</span><span class="sxs-lookup"><span data-stu-id="24dca-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="24dca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24dca-110">PARAMETERS</span></span>

### <span data-ttu-id="24dca-111">-Context</span><span class="sxs-lookup"><span data-stu-id="24dca-111">-Context</span></span>
<span data-ttu-id="24dca-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="24dca-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="24dca-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="24dca-113">This parameter is required.</span></span>

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

### <span data-ttu-id="24dca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24dca-114">-DefaultProfile</span></span>
<span data-ttu-id="24dca-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24dca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24dca-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24dca-116">-PassThru</span></span>
<span data-ttu-id="24dca-117">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="24dca-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="24dca-118">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="24dca-118">-Type</span></span>
<span data-ttu-id="24dca-119">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="24dca-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="24dca-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="24dca-120">This parameter is required.</span></span>

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

### <span data-ttu-id="24dca-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24dca-121">-Confirm</span></span>
<span data-ttu-id="24dca-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24dca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24dca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24dca-123">-WhatIf</span></span>
<span data-ttu-id="24dca-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24dca-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24dca-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24dca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24dca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24dca-126">CommonParameters</span></span>
<span data-ttu-id="24dca-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24dca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24dca-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24dca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24dca-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24dca-129">INPUTS</span></span>

### <span data-ttu-id="24dca-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24dca-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24dca-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="24dca-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="24dca-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24dca-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24dca-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24dca-133">OUTPUTS</span></span>

### <span data-ttu-id="24dca-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24dca-134">System.Boolean</span></span>

## <span data-ttu-id="24dca-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="24dca-135">NOTES</span></span>

## <span data-ttu-id="24dca-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24dca-136">RELATED LINKS</span></span>

[<span data-ttu-id="24dca-137">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="24dca-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="24dca-138">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="24dca-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="24dca-139">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="24dca-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

