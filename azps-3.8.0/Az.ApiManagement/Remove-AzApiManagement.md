---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066676"
---
# <span data-ttu-id="bc556-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bc556-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="bc556-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc556-102">SYNOPSIS</span></span>
<span data-ttu-id="bc556-103">Удаляет службу управления API.</span><span class="sxs-lookup"><span data-stu-id="bc556-103">Removes an API Management service.</span></span>

## <span data-ttu-id="bc556-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc556-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc556-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc556-105">DESCRIPTION</span></span>
<span data-ttu-id="bc556-106">Командлет **Remove-AzApiManagement** Удаляет службу управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="bc556-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="bc556-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc556-107">EXAMPLES</span></span>

### <span data-ttu-id="bc556-108">Пример 1: Удаление службы управления API</span><span class="sxs-lookup"><span data-stu-id="bc556-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="bc556-109">Эта команда удаляет службу управления API с именем ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="bc556-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="bc556-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc556-110">PARAMETERS</span></span>

### <span data-ttu-id="bc556-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc556-111">-DefaultProfile</span></span>
<span data-ttu-id="bc556-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc556-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc556-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc556-113">-Name</span></span>
<span data-ttu-id="bc556-114">Указывает имя развертывания управления API, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bc556-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc556-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc556-115">-PassThru</span></span>
<span data-ttu-id="bc556-116">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bc556-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="bc556-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc556-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc556-118">Указывает имя группы ресурсов, в которой находится развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="bc556-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="bc556-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc556-119">-Confirm</span></span>
<span data-ttu-id="bc556-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc556-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc556-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc556-121">-WhatIf</span></span>
<span data-ttu-id="bc556-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc556-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc556-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc556-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc556-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc556-124">CommonParameters</span></span>
<span data-ttu-id="bc556-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc556-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc556-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc556-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc556-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc556-127">INPUTS</span></span>

### <span data-ttu-id="bc556-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bc556-128">System.String</span></span>

## <span data-ttu-id="bc556-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc556-129">OUTPUTS</span></span>

### <span data-ttu-id="bc556-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc556-130">System.Boolean</span></span>

## <span data-ttu-id="bc556-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc556-131">NOTES</span></span>

## <span data-ttu-id="bc556-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc556-132">RELATED LINKS</span></span>

[<span data-ttu-id="bc556-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bc556-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="bc556-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bc556-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="bc556-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bc556-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="bc556-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bc556-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


