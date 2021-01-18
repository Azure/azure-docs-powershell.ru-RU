---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507161"
---
# <span data-ttu-id="cd7e5-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd7e5-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="cd7e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7e5-103">Удаляет учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-103">Removes an integration account.</span></span>

## <span data-ttu-id="cd7e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd7e5-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd7e5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd7e5-105">DESCRIPTION</span></span>
<span data-ttu-id="cd7e5-106">Для **удаления учетной записи интеграции** из группы ресурсов удаляется учетная запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="cd7e5-107">Укажите имя учетной записи интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="cd7e5-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cd7e5-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cd7e5-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cd7e5-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cd7e5-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd7e5-112">EXAMPLES</span></span>

### <span data-ttu-id="cd7e5-113">Пример 1. Удаление учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="cd7e5-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="cd7e5-114">Эта команда удаляет интеграцию с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="cd7e5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd7e5-115">PARAMETERS</span></span>

### <span data-ttu-id="cd7e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7e5-116">-DefaultProfile</span></span>
<span data-ttu-id="cd7e5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cd7e5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd7e5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cd7e5-118">-Force</span></span>
<span data-ttu-id="cd7e5-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd7e5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cd7e5-120">-Name</span></span>
<span data-ttu-id="cd7e5-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="cd7e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd7e5-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cd7e5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd7e5-124">-Confirm</span></span>
<span data-ttu-id="cd7e5-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd7e5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd7e5-126">-WhatIf</span></span>
<span data-ttu-id="cd7e5-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd7e5-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd7e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7e5-129">CommonParameters</span></span>
<span data-ttu-id="cd7e5-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd7e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7e5-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd7e5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7e5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd7e5-132">INPUTS</span></span>

### <span data-ttu-id="cd7e5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cd7e5-133">System.String</span></span>

## <span data-ttu-id="cd7e5-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd7e5-134">OUTPUTS</span></span>

### <span data-ttu-id="cd7e5-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="cd7e5-135">System.Void</span></span>

## <span data-ttu-id="cd7e5-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd7e5-136">NOTES</span></span>

## <span data-ttu-id="cd7e5-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd7e5-137">RELATED LINKS</span></span>

[<span data-ttu-id="cd7e5-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd7e5-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="cd7e5-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd7e5-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="cd7e5-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd7e5-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


