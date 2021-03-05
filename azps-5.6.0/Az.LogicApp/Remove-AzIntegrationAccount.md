---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: d1f15544223a20113a40975780aa8ca899205f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962003"
---
# <span data-ttu-id="795b0-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="795b0-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="795b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="795b0-102">SYNOPSIS</span></span>
<span data-ttu-id="795b0-103">Удаляет учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="795b0-103">Removes an integration account.</span></span>

## <span data-ttu-id="795b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="795b0-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="795b0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="795b0-105">DESCRIPTION</span></span>
<span data-ttu-id="795b0-106">Для **удаления учетной записи интеграции** из группы ресурсов удаляется учетная запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="795b0-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="795b0-107">Укажите имя учетной записи интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="795b0-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="795b0-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="795b0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="795b0-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="795b0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="795b0-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="795b0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="795b0-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="795b0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="795b0-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="795b0-112">EXAMPLES</span></span>

### <span data-ttu-id="795b0-113">Пример 1. Удаление учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="795b0-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="795b0-114">Эта команда удаляет учетную запись интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="795b0-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="795b0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="795b0-115">PARAMETERS</span></span>

### <span data-ttu-id="795b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795b0-116">-DefaultProfile</span></span>
<span data-ttu-id="795b0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="795b0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="795b0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="795b0-118">-Force</span></span>
<span data-ttu-id="795b0-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="795b0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="795b0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="795b0-120">-Name</span></span>
<span data-ttu-id="795b0-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="795b0-121">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="795b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="795b0-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="795b0-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="795b0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="795b0-124">-Confirm</span></span>
<span data-ttu-id="795b0-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="795b0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="795b0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="795b0-126">-WhatIf</span></span>
<span data-ttu-id="795b0-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="795b0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="795b0-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="795b0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="795b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795b0-129">CommonParameters</span></span>
<span data-ttu-id="795b0-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795b0-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="795b0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795b0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="795b0-132">INPUTS</span></span>

### <span data-ttu-id="795b0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="795b0-133">System.String</span></span>

## <span data-ttu-id="795b0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="795b0-134">OUTPUTS</span></span>

### <span data-ttu-id="795b0-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="795b0-135">System.Void</span></span>

## <span data-ttu-id="795b0-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="795b0-136">NOTES</span></span>

## <span data-ttu-id="795b0-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="795b0-137">RELATED LINKS</span></span>

[<span data-ttu-id="795b0-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="795b0-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="795b0-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="795b0-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="795b0-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="795b0-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


