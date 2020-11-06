---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560583"
---
# <span data-ttu-id="74066-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="74066-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="74066-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74066-102">SYNOPSIS</span></span>
<span data-ttu-id="74066-103">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="74066-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74066-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74066-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74066-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74066-105">DESCRIPTION</span></span>
<span data-ttu-id="74066-106">Удаляет существующую конфигурацию поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="74066-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="74066-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74066-107">EXAMPLES</span></span>

### <span data-ttu-id="74066-108">Удаляет параметры поставщика удостоверений Facebook из службы ApiManagement</span><span class="sxs-lookup"><span data-stu-id="74066-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="74066-109">Удаление конфигурации, связанной с конфигурацией поставщика удостоверений Facebook.</span><span class="sxs-lookup"><span data-stu-id="74066-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="74066-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74066-110">PARAMETERS</span></span>

### <span data-ttu-id="74066-111">-Context</span><span class="sxs-lookup"><span data-stu-id="74066-111">-Context</span></span>
<span data-ttu-id="74066-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="74066-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="74066-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="74066-113">This parameter is required.</span></span>

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

### <span data-ttu-id="74066-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74066-114">-PassThru</span></span>
<span data-ttu-id="74066-115">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="74066-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="74066-116">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="74066-116">-Type</span></span>
<span data-ttu-id="74066-117">Идентификатор существующего поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="74066-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="74066-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="74066-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74066-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74066-119">-Confirm</span></span>
<span data-ttu-id="74066-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74066-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74066-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74066-121">-WhatIf</span></span>
<span data-ttu-id="74066-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74066-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74066-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74066-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74066-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74066-124">-DefaultProfile</span></span>
<span data-ttu-id="74066-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74066-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74066-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74066-126">CommonParameters</span></span>
<span data-ttu-id="74066-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74066-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74066-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74066-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74066-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74066-129">INPUTS</span></span>

## <span data-ttu-id="74066-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74066-130">OUTPUTS</span></span>

### <span data-ttu-id="74066-131">логических</span><span class="sxs-lookup"><span data-stu-id="74066-131">bool</span></span>

## <span data-ttu-id="74066-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="74066-132">NOTES</span></span>

## <span data-ttu-id="74066-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74066-133">RELATED LINKS</span></span>

[<span data-ttu-id="74066-134">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="74066-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="74066-135">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="74066-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="74066-136">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="74066-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

