---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066625"
---
# <span data-ttu-id="50238-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50238-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="50238-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50238-102">SYNOPSIS</span></span>
<span data-ttu-id="50238-103">Удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="50238-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="50238-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50238-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50238-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50238-105">DESCRIPTION</span></span>
<span data-ttu-id="50238-106">Командлет **Remove-AzApiManagementGroup** удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="50238-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="50238-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50238-107">EXAMPLES</span></span>

### <span data-ttu-id="50238-108">Пример 1: удаление существующей группы управления</span><span class="sxs-lookup"><span data-stu-id="50238-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="50238-109">Эта команда удаляет существующую группу управления с именем Group0001 и не запрашивает подтверждение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="50238-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="50238-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50238-110">PARAMETERS</span></span>

### <span data-ttu-id="50238-111">-Context</span><span class="sxs-lookup"><span data-stu-id="50238-111">-Context</span></span>
<span data-ttu-id="50238-112">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="50238-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="50238-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50238-113">-DefaultProfile</span></span>
<span data-ttu-id="50238-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50238-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50238-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="50238-115">-GroupId</span></span>
<span data-ttu-id="50238-116">Указывает идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="50238-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="50238-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50238-117">-PassThru</span></span>
<span data-ttu-id="50238-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="50238-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="50238-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50238-119">-Confirm</span></span>
<span data-ttu-id="50238-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50238-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50238-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50238-121">-WhatIf</span></span>
<span data-ttu-id="50238-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50238-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50238-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50238-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50238-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50238-124">CommonParameters</span></span>
<span data-ttu-id="50238-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50238-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50238-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50238-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50238-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50238-127">INPUTS</span></span>

### <span data-ttu-id="50238-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="50238-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="50238-129">System. String</span><span class="sxs-lookup"><span data-stu-id="50238-129">System.String</span></span>

### <span data-ttu-id="50238-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="50238-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="50238-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50238-131">OUTPUTS</span></span>

### <span data-ttu-id="50238-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50238-132">System.Boolean</span></span>

## <span data-ttu-id="50238-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="50238-133">NOTES</span></span>

## <span data-ttu-id="50238-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50238-134">RELATED LINKS</span></span>

[<span data-ttu-id="50238-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50238-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="50238-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50238-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="50238-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="50238-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


