---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: 73f30ef12270ce738341e71b0428befe6a3a3ba5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901697"
---
# <span data-ttu-id="71ccc-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="71ccc-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="71ccc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="71ccc-103">Удаляет службу управления API.</span><span class="sxs-lookup"><span data-stu-id="71ccc-103">Removes an API Management service.</span></span>

## <span data-ttu-id="71ccc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71ccc-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71ccc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71ccc-105">DESCRIPTION</span></span>
<span data-ttu-id="71ccc-106">Командлет **Remove-AzApiManagement** Удаляет службу управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="71ccc-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="71ccc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71ccc-107">EXAMPLES</span></span>

### <span data-ttu-id="71ccc-108">Пример 1: Удаление службы управления API</span><span class="sxs-lookup"><span data-stu-id="71ccc-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="71ccc-109">Эта команда удаляет службу управления API с именем ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="71ccc-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="71ccc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71ccc-110">PARAMETERS</span></span>

### <span data-ttu-id="71ccc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ccc-111">-DefaultProfile</span></span>
<span data-ttu-id="71ccc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71ccc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ccc-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71ccc-113">-Name</span></span>
<span data-ttu-id="71ccc-114">Указывает имя развертывания управления API, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="71ccc-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71ccc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71ccc-115">-PassThru</span></span>
<span data-ttu-id="71ccc-116">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="71ccc-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="71ccc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ccc-117">-ResourceGroupName</span></span>
<span data-ttu-id="71ccc-118">Указывает имя группы ресурсов, в которой находится развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="71ccc-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="71ccc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71ccc-119">-Confirm</span></span>
<span data-ttu-id="71ccc-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71ccc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71ccc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ccc-121">-WhatIf</span></span>
<span data-ttu-id="71ccc-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71ccc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71ccc-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71ccc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71ccc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ccc-124">CommonParameters</span></span>
<span data-ttu-id="71ccc-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71ccc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ccc-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71ccc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ccc-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71ccc-127">INPUTS</span></span>

### <span data-ttu-id="71ccc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="71ccc-128">System.String</span></span>

## <span data-ttu-id="71ccc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71ccc-129">OUTPUTS</span></span>

### <span data-ttu-id="71ccc-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71ccc-130">System.Boolean</span></span>

## <span data-ttu-id="71ccc-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="71ccc-131">NOTES</span></span>

## <span data-ttu-id="71ccc-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71ccc-132">RELATED LINKS</span></span>

[<span data-ttu-id="71ccc-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="71ccc-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="71ccc-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="71ccc-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="71ccc-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="71ccc-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="71ccc-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="71ccc-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


