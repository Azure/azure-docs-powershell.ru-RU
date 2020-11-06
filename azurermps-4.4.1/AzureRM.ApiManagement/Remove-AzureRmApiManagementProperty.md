---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: 333ed1cb778a5a366a7ad26d426559399658db1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558003"
---
# <span data-ttu-id="cb608-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="cb608-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="cb608-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb608-102">SYNOPSIS</span></span>
<span data-ttu-id="cb608-103">Удаляет свойство управления API.</span><span class="sxs-lookup"><span data-stu-id="cb608-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb608-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb608-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb608-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb608-105">DESCRIPTION</span></span>
<span data-ttu-id="cb608-106">Командлет **Remove-AzureRmApiManagementProperty** удаляет **свойство** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="cb608-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="cb608-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb608-107">EXAMPLES</span></span>

### <span data-ttu-id="cb608-108">Пример 1: Удаление свойства</span><span class="sxs-lookup"><span data-stu-id="cb608-108">Example 1: Remove a property</span></span>
```
PS C:\>Remove-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="cb608-109">Эта команда удаляет свойство с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="cb608-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="cb608-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb608-110">PARAMETERS</span></span>

### <span data-ttu-id="cb608-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cb608-111">-Context</span></span>
<span data-ttu-id="cb608-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cb608-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cb608-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb608-113">-PassThru</span></span>
<span data-ttu-id="cb608-114">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cb608-114">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="cb608-115">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="cb608-115">-PropertyId</span></span>
<span data-ttu-id="cb608-116">Указывает идентификатор свойства, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cb608-116">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cb608-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb608-117">-Confirm</span></span>
<span data-ttu-id="cb608-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb608-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb608-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb608-119">-WhatIf</span></span>
<span data-ttu-id="cb608-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb608-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb608-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb608-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb608-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb608-122">-DefaultProfile</span></span>
<span data-ttu-id="cb608-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb608-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb608-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb608-124">CommonParameters</span></span>
<span data-ttu-id="cb608-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb608-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb608-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb608-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb608-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb608-127">INPUTS</span></span>

## <span data-ttu-id="cb608-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb608-128">OUTPUTS</span></span>

### <span data-ttu-id="cb608-129">логических</span><span class="sxs-lookup"><span data-stu-id="cb608-129">bool</span></span>

## <span data-ttu-id="cb608-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb608-130">NOTES</span></span>

## <span data-ttu-id="cb608-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb608-131">RELATED LINKS</span></span>

[<span data-ttu-id="cb608-132">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="cb608-132">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="cb608-133">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="cb608-133">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


