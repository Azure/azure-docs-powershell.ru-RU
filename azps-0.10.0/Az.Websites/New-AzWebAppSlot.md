---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 41851c1492c3c14e3129ba04367580b09cf3ffb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910586"
---
# <span data-ttu-id="9b4f6-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b4f6-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="9b4f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4f6-103">Создание слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="9b4f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b4f6-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b4f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b4f6-105">DESCRIPTION</span></span>
<span data-ttu-id="9b4f6-106">Командлет **New-AzWebAppSlot** создает слот веб-приложения Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="9b4f6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b4f6-107">EXAMPLES</span></span>

### <span data-ttu-id="9b4f6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b4f6-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="9b4f6-109">Эта команда создает слот с именем Slot001 под существующими именами веб-приложений ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="9b4f6-110">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="9b4f6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b4f6-111">PARAMETERS</span></span>

### <span data-ttu-id="9b4f6-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b4f6-112">-AppServicePlan</span></span>
<span data-ttu-id="9b4f6-113">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="9b4f6-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="9b4f6-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="9b4f6-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="9b4f6-115">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="9b4f6-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="9b4f6-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="9b4f6-116">-AseName</span></span>
<span data-ttu-id="9b4f6-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="9b4f6-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="9b4f6-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4f6-118">-AseResourceGroupName</span></span>
<span data-ttu-id="9b4f6-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="9b4f6-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="9b4f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4f6-120">-DefaultProfile</span></span>
<span data-ttu-id="9b4f6-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4f6-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="9b4f6-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="9b4f6-123">Параметр "пропускать пользовательские HostName"</span><span class="sxs-lookup"><span data-stu-id="9b4f6-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="9b4f6-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="9b4f6-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="9b4f6-125">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="9b4f6-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="9b4f6-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b4f6-126">-Name</span></span>
<span data-ttu-id="9b4f6-127">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="9b4f6-127">Webapp Name</span></span>

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

### <span data-ttu-id="9b4f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b4f6-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9b4f6-129">Resource Group Name</span></span>

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

### <span data-ttu-id="9b4f6-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="9b4f6-130">-Slot</span></span>
<span data-ttu-id="9b4f6-131">Название гнезда webapp</span><span class="sxs-lookup"><span data-stu-id="9b4f6-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="9b4f6-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="9b4f6-132">-SourceWebApp</span></span>
<span data-ttu-id="9b4f6-133">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="9b4f6-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="9b4f6-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b4f6-134">-AsJob</span></span>
<span data-ttu-id="9b4f6-135">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9b4f6-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b4f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4f6-136">CommonParameters</span></span>
<span data-ttu-id="9b4f6-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4f6-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4f6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4f6-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b4f6-139">INPUTS</span></span>

### <span data-ttu-id="9b4f6-140">Семейств</span><span class="sxs-lookup"><span data-stu-id="9b4f6-140">Site</span></span>
<span data-ttu-id="9b4f6-141">Параметр "SourceWebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9b4f6-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9b4f6-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b4f6-142">OUTPUTS</span></span>

## <span data-ttu-id="9b4f6-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b4f6-143">NOTES</span></span>

## <span data-ttu-id="9b4f6-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b4f6-144">RELATED LINKS</span></span>

[<span data-ttu-id="9b4f6-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b4f6-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="9b4f6-146">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b4f6-146">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="9b4f6-147">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b4f6-147">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="9b4f6-148">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b4f6-148">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="9b4f6-149">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b4f6-149">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="9b4f6-150">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9b4f6-150">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="9b4f6-151">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9b4f6-151">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="9b4f6-152">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9b4f6-152">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
