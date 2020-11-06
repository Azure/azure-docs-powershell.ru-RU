---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2fc658f5bab9e6233e6b7279abc0ae80832bcc8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556952"
---
# <span data-ttu-id="08d51-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="08d51-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="08d51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08d51-102">SYNOPSIS</span></span>
<span data-ttu-id="08d51-103">Удаление сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="08d51-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08d51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08d51-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08d51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08d51-105">DESCRIPTION</span></span>
<span data-ttu-id="08d51-106">Командлет **Remove-AzureRmApiManagementAuthorizationServer** удаляет сервер авторизации управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="08d51-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="08d51-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08d51-107">EXAMPLES</span></span>

## <span data-ttu-id="08d51-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08d51-108">PARAMETERS</span></span>

### <span data-ttu-id="08d51-109">-Context</span><span class="sxs-lookup"><span data-stu-id="08d51-109">-Context</span></span>
<span data-ttu-id="08d51-110">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="08d51-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="08d51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d51-111">-DefaultProfile</span></span>
<span data-ttu-id="08d51-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08d51-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08d51-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08d51-113">-PassThru</span></span>
<span data-ttu-id="08d51-114">PassThru</span><span class="sxs-lookup"><span data-stu-id="08d51-114">passthru</span></span>

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

### <span data-ttu-id="08d51-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="08d51-115">-ServerId</span></span>
<span data-ttu-id="08d51-116">Указывает идентификатор сервера авторизации, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="08d51-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="08d51-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08d51-117">-Confirm</span></span>
<span data-ttu-id="08d51-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="08d51-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08d51-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08d51-119">-WhatIf</span></span>
<span data-ttu-id="08d51-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="08d51-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08d51-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="08d51-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08d51-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d51-122">CommonParameters</span></span>
<span data-ttu-id="08d51-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08d51-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d51-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08d51-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d51-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08d51-125">INPUTS</span></span>

### <span data-ttu-id="08d51-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="08d51-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="08d51-127">System. String</span><span class="sxs-lookup"><span data-stu-id="08d51-127">System.String</span></span>

### <span data-ttu-id="08d51-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08d51-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="08d51-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08d51-129">OUTPUTS</span></span>

### <span data-ttu-id="08d51-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08d51-130">System.Boolean</span></span>

## <span data-ttu-id="08d51-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="08d51-131">NOTES</span></span>

## <span data-ttu-id="08d51-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08d51-132">RELATED LINKS</span></span>

[<span data-ttu-id="08d51-133">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="08d51-133">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="08d51-134">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="08d51-134">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="08d51-135">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="08d51-135">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


