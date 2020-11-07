---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: ea063de747f69d10660fe8117d34647156694b5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901634"
---
# <span data-ttu-id="34292-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="34292-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="34292-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34292-102">SYNOPSIS</span></span>
<span data-ttu-id="34292-103">Удаляет свойство управления API.</span><span class="sxs-lookup"><span data-stu-id="34292-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="34292-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34292-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34292-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34292-105">DESCRIPTION</span></span>
<span data-ttu-id="34292-106">Командлет **Remove-AzApiManagementProperty** удаляет **свойство** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="34292-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="34292-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34292-107">EXAMPLES</span></span>

### <span data-ttu-id="34292-108">Пример 1: Удаление свойства</span><span class="sxs-lookup"><span data-stu-id="34292-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="34292-109">Эта команда удаляет свойство с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="34292-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="34292-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34292-110">PARAMETERS</span></span>

### <span data-ttu-id="34292-111">-Context</span><span class="sxs-lookup"><span data-stu-id="34292-111">-Context</span></span>
<span data-ttu-id="34292-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="34292-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="34292-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34292-113">-DefaultProfile</span></span>
<span data-ttu-id="34292-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34292-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34292-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34292-115">-PassThru</span></span>
<span data-ttu-id="34292-116">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="34292-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="34292-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="34292-117">-PropertyId</span></span>
<span data-ttu-id="34292-118">Указывает идентификатор свойства, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="34292-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34292-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34292-119">-Confirm</span></span>
<span data-ttu-id="34292-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34292-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34292-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34292-121">-WhatIf</span></span>
<span data-ttu-id="34292-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34292-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34292-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34292-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34292-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34292-124">CommonParameters</span></span>
<span data-ttu-id="34292-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34292-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34292-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34292-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34292-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34292-127">INPUTS</span></span>

### <span data-ttu-id="34292-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="34292-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="34292-129">System. String</span><span class="sxs-lookup"><span data-stu-id="34292-129">System.String</span></span>

### <span data-ttu-id="34292-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="34292-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="34292-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34292-131">OUTPUTS</span></span>

### <span data-ttu-id="34292-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34292-132">System.Boolean</span></span>

## <span data-ttu-id="34292-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="34292-133">NOTES</span></span>

## <span data-ttu-id="34292-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34292-134">RELATED LINKS</span></span>

[<span data-ttu-id="34292-135">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="34292-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="34292-136">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="34292-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


