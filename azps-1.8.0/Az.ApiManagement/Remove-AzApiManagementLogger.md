---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: d5f04c44638f5aa0cfc34ca528d57fca8afe5b08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901658"
---
# <span data-ttu-id="6a3b4-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6a3b4-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="6a3b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3b4-103">Удаляет средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="6a3b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a3b4-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a3b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a3b4-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3b4-106">Командлет **Remove-AzApiManagementLogger** удаляет **средство ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="6a3b4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a3b4-107">EXAMPLES</span></span>

### <span data-ttu-id="6a3b4-108">Пример 1: удаление средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="6a3b4-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="6a3b4-109">Эта команда удаляет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="6a3b4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a3b4-110">PARAMETERS</span></span>

### <span data-ttu-id="6a3b4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6a3b4-111">-Context</span></span>
<span data-ttu-id="6a3b4-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6a3b4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6a3b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3b4-113">-DefaultProfile</span></span>
<span data-ttu-id="6a3b4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3b4-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="6a3b4-115">-LoggerId</span></span>
<span data-ttu-id="6a3b4-116">Указывает идентификатор средства ведения журнала, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="6a3b4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a3b4-117">-PassThru</span></span>
<span data-ttu-id="6a3b4-118">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="6a3b4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a3b4-119">-Confirm</span></span>
<span data-ttu-id="6a3b4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a3b4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a3b4-121">-WhatIf</span></span>
<span data-ttu-id="6a3b4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a3b4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a3b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3b4-124">CommonParameters</span></span>
<span data-ttu-id="6a3b4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a3b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3b4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a3b4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3b4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a3b4-127">INPUTS</span></span>

### <span data-ttu-id="6a3b4-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6a3b4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6a3b4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6a3b4-129">System.String</span></span>

### <span data-ttu-id="6a3b4-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6a3b4-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6a3b4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a3b4-131">OUTPUTS</span></span>

### <span data-ttu-id="6a3b4-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a3b4-132">System.Boolean</span></span>

## <span data-ttu-id="6a3b4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a3b4-133">NOTES</span></span>

## <span data-ttu-id="6a3b4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a3b4-134">RELATED LINKS</span></span>

[<span data-ttu-id="6a3b4-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6a3b4-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="6a3b4-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6a3b4-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="6a3b4-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6a3b4-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


