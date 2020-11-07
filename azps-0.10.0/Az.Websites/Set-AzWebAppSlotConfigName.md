---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: ab00a1fbafc446affd30d7ae06dd0d48f0f0d04d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910564"
---
# <span data-ttu-id="4f4cd-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="4f4cd-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="4f4cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4cd-103">Настройка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="4f4cd-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="4f4cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f4cd-104">SYNTAX</span></span>

### <span data-ttu-id="4f4cd-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="4f4cd-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f4cd-106">S2</span><span class="sxs-lookup"><span data-stu-id="4f4cd-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f4cd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f4cd-107">DESCRIPTION</span></span>
<span data-ttu-id="4f4cd-108">Командлет **Set-AzWebAppSlotConfigName** отмечает параметры приложения и строки соединения в качестве параметров слота.</span><span class="sxs-lookup"><span data-stu-id="4f4cd-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="4f4cd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f4cd-109">EXAMPLES</span></span>

### <span data-ttu-id="4f4cd-110">1:</span><span class="sxs-lookup"><span data-stu-id="4f4cd-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="4f4cd-111">Эта команда удаляет все параметры приложения и строки подключения для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="4f4cd-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4f4cd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f4cd-112">PARAMETERS</span></span>

### <span data-ttu-id="4f4cd-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="4f4cd-113">-AppSettingNames</span></span>
<span data-ttu-id="4f4cd-114">Массив строк с именами параметров приложения</span><span class="sxs-lookup"><span data-stu-id="4f4cd-114">App Settings Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4cd-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="4f4cd-115">-ConnectionStringNames</span></span>
<span data-ttu-id="4f4cd-116">Массив строк соединения с именами строк</span><span class="sxs-lookup"><span data-stu-id="4f4cd-116">Connection String Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4cd-117">-DefaultProfile</span></span>
<span data-ttu-id="4f4cd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4cd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f4cd-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4f4cd-119">-Name</span></span>
<span data-ttu-id="4f4cd-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="4f4cd-120">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4cd-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="4f4cd-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="4f4cd-122">Параметр "удалить все имена параметров приложений"</span><span class="sxs-lookup"><span data-stu-id="4f4cd-122">Remove All App Setting Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4cd-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="4f4cd-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="4f4cd-124">Параметр "удалить все имена строк подключения"</span><span class="sxs-lookup"><span data-stu-id="4f4cd-124">Remove All Connection String Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f4cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f4cd-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4f4cd-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4cd-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4f4cd-127">-WebApp</span></span>
<span data-ttu-id="4f4cd-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="4f4cd-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4cd-129">CommonParameters</span></span>
<span data-ttu-id="4f4cd-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f4cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4cd-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4cd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4cd-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f4cd-132">INPUTS</span></span>

### <span data-ttu-id="4f4cd-133">Семейств</span><span class="sxs-lookup"><span data-stu-id="4f4cd-133">Site</span></span>
<span data-ttu-id="4f4cd-134">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4f4cd-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4f4cd-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f4cd-135">OUTPUTS</span></span>

## <span data-ttu-id="4f4cd-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f4cd-136">NOTES</span></span>

## <span data-ttu-id="4f4cd-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f4cd-137">RELATED LINKS</span></span>

