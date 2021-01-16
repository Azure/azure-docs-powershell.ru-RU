---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403652"
---
# <span data-ttu-id="65abc-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65abc-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="65abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65abc-102">SYNOPSIS</span></span>
<span data-ttu-id="65abc-103">Удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="65abc-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="65abc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65abc-104">SYNTAX</span></span>

### <span data-ttu-id="65abc-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65abc-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65abc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65abc-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65abc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65abc-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65abc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65abc-108">DESCRIPTION</span></span>
<span data-ttu-id="65abc-109">С **его учетной** записью будет удалена существующая подписка.</span><span class="sxs-lookup"><span data-stu-id="65abc-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="65abc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65abc-110">EXAMPLES</span></span>

### <span data-ttu-id="65abc-111">Пример 1. Удаление подписки</span><span class="sxs-lookup"><span data-stu-id="65abc-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="65abc-112">Эта команда удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="65abc-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="65abc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65abc-113">PARAMETERS</span></span>

### <span data-ttu-id="65abc-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="65abc-114">-Context</span></span>
<span data-ttu-id="65abc-115">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="65abc-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="65abc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65abc-116">-DefaultProfile</span></span>
<span data-ttu-id="65abc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65abc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65abc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65abc-118">-InputObject</span></span>
<span data-ttu-id="65abc-119">Экземпляр PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="65abc-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="65abc-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="65abc-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65abc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65abc-121">-PassThru</span></span>
<span data-ttu-id="65abc-122">Указывает на то, что этот $True возвращает значение $True, если он успешно, или значение $false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="65abc-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="65abc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65abc-123">-ResourceId</span></span>
<span data-ttu-id="65abc-124">Arm ResourceId подписки.</span><span class="sxs-lookup"><span data-stu-id="65abc-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="65abc-125">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="65abc-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65abc-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65abc-126">-SubscriptionId</span></span>
<span data-ttu-id="65abc-127">Определяет ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="65abc-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="65abc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65abc-128">-Confirm</span></span>
<span data-ttu-id="65abc-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65abc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65abc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65abc-130">-WhatIf</span></span>
<span data-ttu-id="65abc-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65abc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65abc-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="65abc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65abc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65abc-133">CommonParameters</span></span>
<span data-ttu-id="65abc-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65abc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65abc-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65abc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65abc-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65abc-136">INPUTS</span></span>

### <span data-ttu-id="65abc-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="65abc-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="65abc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="65abc-138">System.String</span></span>

### <span data-ttu-id="65abc-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="65abc-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="65abc-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65abc-140">OUTPUTS</span></span>

### <span data-ttu-id="65abc-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65abc-141">System.Boolean</span></span>

## <span data-ttu-id="65abc-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65abc-142">NOTES</span></span>

## <span data-ttu-id="65abc-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65abc-143">RELATED LINKS</span></span>

[<span data-ttu-id="65abc-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65abc-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="65abc-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65abc-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="65abc-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="65abc-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


