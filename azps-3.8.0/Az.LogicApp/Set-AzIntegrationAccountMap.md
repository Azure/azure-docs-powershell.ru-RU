---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: 774fab39542c97dfdd34dbbad672c1dd6b1debc6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064902"
---
# <span data-ttu-id="5bced-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bced-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="5bced-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5bced-102">SYNOPSIS</span></span>
<span data-ttu-id="5bced-103">Изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="5bced-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5bced-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bced-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bced-105">DESCRIPTION</span></span>
<span data-ttu-id="5bced-106">Командлет **Set-AzIntegrationAccountMap** изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="5bced-107">Этот командлет возвращает объект, представляющий карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="5bced-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="5bced-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="5bced-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="5bced-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5bced-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="5bced-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5bced-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="5bced-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5bced-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="5bced-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5bced-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5bced-113">EXAMPLES</span></span>

### <span data-ttu-id="5bced-114">Пример 1: изменение карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="5bced-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="5bced-115">Эта команда изменяет карту учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bced-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="5bced-116">Команда задает определение карты, которое хранится в переменной $MapContent с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="5bced-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="5bced-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5bced-117">PARAMETERS</span></span>

### <span data-ttu-id="5bced-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="5bced-118">-ContentType</span></span>
<span data-ttu-id="5bced-119">Указывает тип контента для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="5bced-120">Этот командлет поддерживает приложение и XML в качестве типа контента "карта".</span><span class="sxs-lookup"><span data-stu-id="5bced-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bced-121">-DefaultProfile</span></span>
<span data-ttu-id="5bced-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5bced-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bced-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5bced-123">-Force</span></span>
<span data-ttu-id="5bced-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5bced-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5bced-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="5bced-125">-MapDefinition</span></span>
<span data-ttu-id="5bced-126">Указывает объект определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-126">Specifies a definition object for integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="5bced-127">-MapFilePath</span></span>
<span data-ttu-id="5bced-128">Задает путь к файлу определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-128">Specifies the file path of a definition for the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="5bced-129">-MapName</span></span>
<span data-ttu-id="5bced-130">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-130">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="5bced-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="5bced-131">-MapType</span></span>
<span data-ttu-id="5bced-132">Указывает тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="5bced-133">Этот командлет поддерживает преобразование XSLT в тип карты.</span><span class="sxs-lookup"><span data-stu-id="5bced-133">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5bced-134">-Metadata</span></span>
<span data-ttu-id="5bced-135">Указывает объект метаданных для карты.</span><span class="sxs-lookup"><span data-stu-id="5bced-135">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5bced-136">-Name</span></span>
<span data-ttu-id="5bced-137">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="5bced-137">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bced-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bced-138">-ResourceGroupName</span></span>
<span data-ttu-id="5bced-139">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bced-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5bced-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bced-140">-Confirm</span></span>
<span data-ttu-id="5bced-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5bced-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bced-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bced-142">-WhatIf</span></span>
<span data-ttu-id="5bced-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5bced-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bced-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5bced-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bced-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bced-145">CommonParameters</span></span>
<span data-ttu-id="5bced-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5bced-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bced-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bced-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bced-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5bced-148">INPUTS</span></span>

### <span data-ttu-id="5bced-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5bced-149">System.String</span></span>

## <span data-ttu-id="5bced-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bced-150">OUTPUTS</span></span>

### <span data-ttu-id="5bced-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bced-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="5bced-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="5bced-152">NOTES</span></span>

## <span data-ttu-id="5bced-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bced-153">RELATED LINKS</span></span>

[<span data-ttu-id="5bced-154">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bced-154">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="5bced-155">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bced-155">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="5bced-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="5bced-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


