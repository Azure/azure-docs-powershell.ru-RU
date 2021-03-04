---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: daa4169ed077003d2ceb773e2e085e72fb6d1ec8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959155"
---
# <span data-ttu-id="89bcb-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="89bcb-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="89bcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="89bcb-103">Удаляет службу управления API.</span><span class="sxs-lookup"><span data-stu-id="89bcb-103">Removes an API Management service.</span></span>

## <span data-ttu-id="89bcb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89bcb-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89bcb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89bcb-105">DESCRIPTION</span></span>
<span data-ttu-id="89bcb-106">**Из-за выполнения команды Remove-AzApiManagement** служба управления API Azure удаляется.</span><span class="sxs-lookup"><span data-stu-id="89bcb-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="89bcb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89bcb-107">EXAMPLES</span></span>

### <span data-ttu-id="89bcb-108">Пример 1. Удаление службы управления API</span><span class="sxs-lookup"><span data-stu-id="89bcb-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="89bcb-109">Эта команда удаляет службу управления API под названием ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="89bcb-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="89bcb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89bcb-110">PARAMETERS</span></span>

### <span data-ttu-id="89bcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bcb-111">-DefaultProfile</span></span>
<span data-ttu-id="89bcb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89bcb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89bcb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="89bcb-113">-Name</span></span>
<span data-ttu-id="89bcb-114">Указывает имя развертывания управления API, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89bcb-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89bcb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89bcb-115">-PassThru</span></span>
<span data-ttu-id="89bcb-116">Указывает на то, что этот $True возвращает значение, если операция будет успешной.</span><span class="sxs-lookup"><span data-stu-id="89bcb-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89bcb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89bcb-117">-ResourceGroupName</span></span>
<span data-ttu-id="89bcb-118">Имя группы ресурсов, в которой развернуто управление API.</span><span class="sxs-lookup"><span data-stu-id="89bcb-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="89bcb-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89bcb-119">-Confirm</span></span>
<span data-ttu-id="89bcb-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89bcb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89bcb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89bcb-121">-WhatIf</span></span>
<span data-ttu-id="89bcb-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89bcb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89bcb-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89bcb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89bcb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bcb-124">CommonParameters</span></span>
<span data-ttu-id="89bcb-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89bcb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bcb-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89bcb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bcb-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89bcb-127">INPUTS</span></span>

### <span data-ttu-id="89bcb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="89bcb-128">System.String</span></span>

## <span data-ttu-id="89bcb-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89bcb-129">OUTPUTS</span></span>

### <span data-ttu-id="89bcb-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89bcb-130">System.Boolean</span></span>

## <span data-ttu-id="89bcb-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89bcb-131">NOTES</span></span>

## <span data-ttu-id="89bcb-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89bcb-132">RELATED LINKS</span></span>

[<span data-ttu-id="89bcb-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="89bcb-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="89bcb-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="89bcb-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="89bcb-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="89bcb-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="89bcb-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="89bcb-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


