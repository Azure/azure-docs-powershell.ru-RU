---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066667"
---
# <span data-ttu-id="f1520-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f1520-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="f1520-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1520-102">SYNOPSIS</span></span>
<span data-ttu-id="f1520-103">Удаляет API.</span><span class="sxs-lookup"><span data-stu-id="f1520-103">Removes an API.</span></span>

## <span data-ttu-id="f1520-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1520-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1520-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1520-105">DESCRIPTION</span></span>
<span data-ttu-id="f1520-106">Командлет **Remove-AzApiManagementApi** УДАЛЯЕТ существующий API.</span><span class="sxs-lookup"><span data-stu-id="f1520-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="f1520-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1520-107">EXAMPLES</span></span>

### <span data-ttu-id="f1520-108">Пример 1: удаление API</span><span class="sxs-lookup"><span data-stu-id="f1520-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="f1520-109">Эта команда удаляет API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="f1520-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="f1520-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1520-110">PARAMETERS</span></span>

### <span data-ttu-id="f1520-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f1520-111">-ApiId</span></span>
<span data-ttu-id="f1520-112">Указывает идентификатор API Remove.</span><span class="sxs-lookup"><span data-stu-id="f1520-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="f1520-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f1520-113">-Context</span></span>
<span data-ttu-id="f1520-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f1520-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f1520-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1520-115">-DefaultProfile</span></span>
<span data-ttu-id="f1520-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1520-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1520-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1520-117">-PassThru</span></span>
<span data-ttu-id="f1520-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="f1520-118">passthru</span></span>

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

### <span data-ttu-id="f1520-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1520-119">-Confirm</span></span>
<span data-ttu-id="f1520-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1520-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1520-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1520-121">-WhatIf</span></span>
<span data-ttu-id="f1520-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1520-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1520-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1520-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1520-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1520-124">CommonParameters</span></span>
<span data-ttu-id="f1520-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1520-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1520-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1520-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1520-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1520-127">INPUTS</span></span>

### <span data-ttu-id="f1520-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1520-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1520-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f1520-129">System.String</span></span>

### <span data-ttu-id="f1520-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1520-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1520-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1520-131">OUTPUTS</span></span>

### <span data-ttu-id="f1520-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1520-132">System.Boolean</span></span>

## <span data-ttu-id="f1520-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1520-133">NOTES</span></span>

## <span data-ttu-id="f1520-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1520-134">RELATED LINKS</span></span>

[<span data-ttu-id="f1520-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f1520-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="f1520-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f1520-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="f1520-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f1520-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="f1520-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f1520-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="f1520-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f1520-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


