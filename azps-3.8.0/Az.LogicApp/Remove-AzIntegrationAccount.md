---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065865"
---
# <span data-ttu-id="d2ee1-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d2ee1-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="d2ee1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ee1-103">Удаление учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-103">Removes an integration account.</span></span>

## <span data-ttu-id="d2ee1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2ee1-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ee1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ee1-106">Командлет **Remove-AzIntegrationAccount** удаляет учетную запись интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="d2ee1-107">Укажите имя учетной записи для интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="d2ee1-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d2ee1-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d2ee1-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d2ee1-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d2ee1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2ee1-112">EXAMPLES</span></span>

### <span data-ttu-id="d2ee1-113">Пример 1: Удаление учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="d2ee1-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="d2ee1-114">Эта команда удаляет учетную запись интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="d2ee1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2ee1-115">PARAMETERS</span></span>

### <span data-ttu-id="d2ee1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ee1-116">-DefaultProfile</span></span>
<span data-ttu-id="d2ee1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2ee1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2ee1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d2ee1-118">-Force</span></span>
<span data-ttu-id="d2ee1-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2ee1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2ee1-120">-Name</span></span>
<span data-ttu-id="d2ee1-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="d2ee1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ee1-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2ee1-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d2ee1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2ee1-124">-Confirm</span></span>
<span data-ttu-id="d2ee1-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ee1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ee1-126">-WhatIf</span></span>
<span data-ttu-id="d2ee1-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ee1-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ee1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ee1-129">CommonParameters</span></span>
<span data-ttu-id="d2ee1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2ee1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ee1-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ee1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ee1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2ee1-132">INPUTS</span></span>

### <span data-ttu-id="d2ee1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ee1-133">System.String</span></span>

## <span data-ttu-id="d2ee1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ee1-134">OUTPUTS</span></span>

### <span data-ttu-id="d2ee1-135">System. void</span><span class="sxs-lookup"><span data-stu-id="d2ee1-135">System.Void</span></span>

## <span data-ttu-id="d2ee1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2ee1-136">NOTES</span></span>

## <span data-ttu-id="d2ee1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2ee1-137">RELATED LINKS</span></span>

[<span data-ttu-id="d2ee1-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d2ee1-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="d2ee1-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d2ee1-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="d2ee1-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d2ee1-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


