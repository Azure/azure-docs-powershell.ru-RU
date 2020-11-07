---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: f41149c6abb946340acc06b847c72dcabcee18fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913710"
---
# <span data-ttu-id="b4285-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4285-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="b4285-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4285-102">SYNOPSIS</span></span>
<span data-ttu-id="b4285-103">Создание слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b4285-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4285-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4285-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4285-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4285-105">DESCRIPTION</span></span>
<span data-ttu-id="b4285-106">Командлет **New-AzureRmWebAppSlot** создает слот веб-приложения Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="b4285-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="b4285-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4285-107">EXAMPLES</span></span>

### <span data-ttu-id="b4285-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4285-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="b4285-109">Эта команда создает слот с именем Slot001 под существующими именами веб-приложений ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="b4285-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="b4285-110">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b4285-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="b4285-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4285-111">PARAMETERS</span></span>

### <span data-ttu-id="b4285-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b4285-112">-AppServicePlan</span></span>
<span data-ttu-id="b4285-113">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="b4285-113">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="b4285-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="b4285-115">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="b4285-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="b4285-116">-AseName</span></span>
<span data-ttu-id="b4285-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="b4285-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4285-118">-AseResourceGroupName</span></span>
<span data-ttu-id="b4285-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="b4285-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4285-120">-DefaultProfile</span></span>
<span data-ttu-id="b4285-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4285-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4285-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="b4285-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="b4285-123">Параметр "пропускать пользовательские HostName"</span><span class="sxs-lookup"><span data-stu-id="b4285-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="b4285-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="b4285-125">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="b4285-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4285-126">-Name</span></span>
<span data-ttu-id="b4285-127">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="b4285-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4285-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4285-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b4285-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="b4285-130">-Slot</span></span>
<span data-ttu-id="b4285-131">Название гнезда webapp</span><span class="sxs-lookup"><span data-stu-id="b4285-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="b4285-132">-SourceWebApp</span></span>
<span data-ttu-id="b4285-133">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="b4285-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4285-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4285-134">-AsJob</span></span>
<span data-ttu-id="b4285-135">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b4285-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4285-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4285-136">CommonParameters</span></span>
<span data-ttu-id="b4285-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4285-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4285-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4285-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4285-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4285-139">INPUTS</span></span>

### <span data-ttu-id="b4285-140">Семейств</span><span class="sxs-lookup"><span data-stu-id="b4285-140">Site</span></span>
<span data-ttu-id="b4285-141">Параметр "SourceWebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b4285-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b4285-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4285-142">OUTPUTS</span></span>

## <span data-ttu-id="b4285-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4285-143">NOTES</span></span>

## <span data-ttu-id="b4285-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4285-144">RELATED LINKS</span></span>

[<span data-ttu-id="b4285-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4285-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="b4285-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4285-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="b4285-147">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4285-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="b4285-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4285-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="b4285-149">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4285-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="b4285-150">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b4285-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="b4285-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b4285-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="b4285-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b4285-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
