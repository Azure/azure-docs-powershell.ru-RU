---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cf27d54e50d320d0ad20a3e847cf2b9dda8ac3c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566854"
---
# <span data-ttu-id="eac55-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eac55-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="eac55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eac55-102">SYNOPSIS</span></span>
<span data-ttu-id="eac55-103">Удаляет API.</span><span class="sxs-lookup"><span data-stu-id="eac55-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eac55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eac55-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac55-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac55-105">DESCRIPTION</span></span>
<span data-ttu-id="eac55-106">Командлет **Remove-AzureRmApiManagementApi** УДАЛЯЕТ существующий API.</span><span class="sxs-lookup"><span data-stu-id="eac55-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="eac55-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eac55-107">EXAMPLES</span></span>

### <span data-ttu-id="eac55-108">Пример 1: удаление API</span><span class="sxs-lookup"><span data-stu-id="eac55-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="eac55-109">Эта команда удаляет API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="eac55-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="eac55-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eac55-110">PARAMETERS</span></span>

### <span data-ttu-id="eac55-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="eac55-111">-ApiId</span></span>
<span data-ttu-id="eac55-112">Указывает идентификатор API Remove.</span><span class="sxs-lookup"><span data-stu-id="eac55-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="eac55-113">-Context</span><span class="sxs-lookup"><span data-stu-id="eac55-113">-Context</span></span>
<span data-ttu-id="eac55-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="eac55-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eac55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac55-115">-DefaultProfile</span></span>
<span data-ttu-id="eac55-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eac55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eac55-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eac55-117">-PassThru</span></span>
<span data-ttu-id="eac55-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="eac55-118">passthru</span></span>

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

### <span data-ttu-id="eac55-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eac55-119">-Confirm</span></span>
<span data-ttu-id="eac55-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eac55-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac55-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac55-121">-WhatIf</span></span>
<span data-ttu-id="eac55-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eac55-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac55-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eac55-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac55-124">CommonParameters</span></span>
<span data-ttu-id="eac55-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eac55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac55-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eac55-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac55-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eac55-127">INPUTS</span></span>

### <span data-ttu-id="eac55-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eac55-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eac55-129">System. String</span><span class="sxs-lookup"><span data-stu-id="eac55-129">System.String</span></span>

### <span data-ttu-id="eac55-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eac55-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eac55-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac55-131">OUTPUTS</span></span>

### <span data-ttu-id="eac55-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eac55-132">System.Boolean</span></span>

## <span data-ttu-id="eac55-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="eac55-133">NOTES</span></span>

## <span data-ttu-id="eac55-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eac55-134">RELATED LINKS</span></span>

[<span data-ttu-id="eac55-135">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eac55-135">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="eac55-136">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eac55-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="eac55-137">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eac55-137">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="eac55-138">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eac55-138">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="eac55-139">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="eac55-139">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


