---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224388"
---
# <span data-ttu-id="1247a-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="1247a-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="1247a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1247a-102">SYNOPSIS</span></span>
<span data-ttu-id="1247a-103">Получает URL-адрес запуска логики приложения для вызовите звонок.</span><span class="sxs-lookup"><span data-stu-id="1247a-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="1247a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1247a-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1247a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1247a-105">DESCRIPTION</span></span>
<span data-ttu-id="1247a-106">**Cmdlet Get-AzLogicAppTriggerCallbackUrl получает URL-адрес** вызываемого триггера приложения "Логика" из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1247a-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="1247a-107">Этот cmdlet возвращает объект **WorkflowTriggerCallbackUrl,** представляютый URL-адресом обратного звонка.</span><span class="sxs-lookup"><span data-stu-id="1247a-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="1247a-108">Укажите имя группы ресурсов, имя приложения логики и имя триггера.</span><span class="sxs-lookup"><span data-stu-id="1247a-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="1247a-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="1247a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1247a-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="1247a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1247a-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="1247a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1247a-112">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="1247a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1247a-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1247a-113">EXAMPLES</span></span>

### <span data-ttu-id="1247a-114">Пример 1. Получить URL-адрес триггера воспроизведения в приложении "Логика"</span><span class="sxs-lookup"><span data-stu-id="1247a-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="1247a-115">Эта команда получает URL-адрес запуска приложения для логики.</span><span class="sxs-lookup"><span data-stu-id="1247a-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="1247a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1247a-116">PARAMETERS</span></span>

### <span data-ttu-id="1247a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1247a-117">-DefaultProfile</span></span>
<span data-ttu-id="1247a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1247a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1247a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1247a-119">-Name</span></span>
<span data-ttu-id="1247a-120">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="1247a-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1247a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1247a-121">-ResourceGroupName</span></span>
<span data-ttu-id="1247a-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1247a-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1247a-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="1247a-123">-TriggerName</span></span>
<span data-ttu-id="1247a-124">Указывает имя триггера.</span><span class="sxs-lookup"><span data-stu-id="1247a-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="1247a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1247a-125">CommonParameters</span></span>
<span data-ttu-id="1247a-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1247a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1247a-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1247a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1247a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1247a-128">INPUTS</span></span>

### <span data-ttu-id="1247a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1247a-129">System.String</span></span>

## <span data-ttu-id="1247a-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1247a-130">OUTPUTS</span></span>

### <span data-ttu-id="1247a-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="1247a-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="1247a-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1247a-132">NOTES</span></span>

## <span data-ttu-id="1247a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1247a-133">RELATED LINKS</span></span>

[<span data-ttu-id="1247a-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="1247a-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


