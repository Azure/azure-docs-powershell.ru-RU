---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 04cd6204b93a0ce84f025d6af931c5f5e287c558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566157"
---
# <span data-ttu-id="f052a-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f052a-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="f052a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f052a-102">SYNOPSIS</span></span>
<span data-ttu-id="f052a-103">Изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f052a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f052a-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f052a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f052a-105">DESCRIPTION</span></span>
<span data-ttu-id="f052a-106">Командлет **Set-AzureRmIntegrationAccountMap** изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="f052a-107">Этот командлет возвращает объект, представляющий карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="f052a-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="f052a-108">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="f052a-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="f052a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f052a-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="f052a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f052a-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f052a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f052a-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f052a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f052a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f052a-113">EXAMPLES</span></span>

### <span data-ttu-id="f052a-114">Пример 1: изменение карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="f052a-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="f052a-115">Эта команда изменяет карту учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f052a-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="f052a-116">Команда задает определение карты, которое хранится в переменной $MapContent с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="f052a-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="f052a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f052a-117">PARAMETERS</span></span>

### <span data-ttu-id="f052a-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="f052a-118">-ContentType</span></span>
<span data-ttu-id="f052a-119">Указывает тип контента для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="f052a-120">Этот командлет поддерживает приложение и XML в качестве типа контента "карта".</span><span class="sxs-lookup"><span data-stu-id="f052a-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f052a-121">-DefaultProfile</span></span>
<span data-ttu-id="f052a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f052a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f052a-123">-Force</span></span>
<span data-ttu-id="f052a-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f052a-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="f052a-125">-MapDefinition</span></span>
<span data-ttu-id="f052a-126">Указывает объект определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-126">Specifies a definition object for integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="f052a-127">-MapFilePath</span></span>
<span data-ttu-id="f052a-128">Задает путь к файлу определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-128">Specifies the file path of a definition for the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="f052a-129">-MapName</span></span>
<span data-ttu-id="f052a-130">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-130">Specifies the name of an integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="f052a-131">-MapType</span></span>
<span data-ttu-id="f052a-132">Указывает тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="f052a-133">Этот командлет поддерживает преобразование XSLT в тип карты.</span><span class="sxs-lookup"><span data-stu-id="f052a-133">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f052a-134">-Metadata</span></span>
<span data-ttu-id="f052a-135">Указывает объект метаданных для карты.</span><span class="sxs-lookup"><span data-stu-id="f052a-135">Specifies a metadata object for the map.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f052a-136">-Name</span></span>
<span data-ttu-id="f052a-137">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f052a-137">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f052a-138">-ResourceGroupName</span></span>
<span data-ttu-id="f052a-139">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f052a-139">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f052a-140">-Confirm</span></span>
<span data-ttu-id="f052a-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f052a-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f052a-142">-WhatIf</span></span>
<span data-ttu-id="f052a-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f052a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f052a-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f052a-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f052a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f052a-145">CommonParameters</span></span>
<span data-ttu-id="f052a-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f052a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f052a-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f052a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f052a-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f052a-148">INPUTS</span></span>

### <span data-ttu-id="f052a-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="f052a-149">None</span></span>
<span data-ttu-id="f052a-150">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f052a-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f052a-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f052a-151">OUTPUTS</span></span>

### <span data-ttu-id="f052a-152">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f052a-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="f052a-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="f052a-153">NOTES</span></span>

## <span data-ttu-id="f052a-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f052a-154">RELATED LINKS</span></span>

[<span data-ttu-id="f052a-155">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f052a-155">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="f052a-156">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f052a-156">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="f052a-157">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f052a-157">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)


