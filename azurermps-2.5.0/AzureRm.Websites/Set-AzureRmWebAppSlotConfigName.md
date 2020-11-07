---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: 39c3ce693a1ee17a5b547c027ab9165388fe10f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914334"
---
# <span data-ttu-id="73e48-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="73e48-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="73e48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73e48-102">SYNOPSIS</span></span>
<span data-ttu-id="73e48-103">Настройка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="73e48-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73e48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73e48-104">SYNTAX</span></span>

### <span data-ttu-id="73e48-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="73e48-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73e48-106">S2</span><span class="sxs-lookup"><span data-stu-id="73e48-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73e48-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73e48-107">DESCRIPTION</span></span>
<span data-ttu-id="73e48-108">Командлет **Set-AzureRmWebAppSlotConfigName** отмечает параметры приложения и строки соединения в качестве параметров слота.</span><span class="sxs-lookup"><span data-stu-id="73e48-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="73e48-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73e48-109">EXAMPLES</span></span>

### <span data-ttu-id="73e48-110">1:</span><span class="sxs-lookup"><span data-stu-id="73e48-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="73e48-111">Эта команда удаляет все параметры приложения и строки подключения для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="73e48-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="73e48-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73e48-112">PARAMETERS</span></span>

### <span data-ttu-id="73e48-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="73e48-113">-AppSettingNames</span></span>
<span data-ttu-id="73e48-114">Массив строк с именами параметров приложения</span><span class="sxs-lookup"><span data-stu-id="73e48-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="73e48-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="73e48-115">-ConnectionStringNames</span></span>
<span data-ttu-id="73e48-116">Массив строк соединения с именами строк</span><span class="sxs-lookup"><span data-stu-id="73e48-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="73e48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e48-117">-DefaultProfile</span></span>
<span data-ttu-id="73e48-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73e48-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73e48-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73e48-119">-Name</span></span>
<span data-ttu-id="73e48-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="73e48-120">WebApp Name</span></span>

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

### <span data-ttu-id="73e48-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="73e48-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="73e48-122">Параметр "удалить все имена параметров приложений"</span><span class="sxs-lookup"><span data-stu-id="73e48-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="73e48-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="73e48-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="73e48-124">Параметр "удалить все имена строк подключения"</span><span class="sxs-lookup"><span data-stu-id="73e48-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="73e48-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e48-125">-ResourceGroupName</span></span>
<span data-ttu-id="73e48-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="73e48-126">Resource Group Name</span></span>

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

### <span data-ttu-id="73e48-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="73e48-127">-WebApp</span></span>
<span data-ttu-id="73e48-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="73e48-128">WebApp Object</span></span>

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

### <span data-ttu-id="73e48-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e48-129">CommonParameters</span></span>
<span data-ttu-id="73e48-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73e48-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e48-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e48-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e48-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73e48-132">INPUTS</span></span>

### <span data-ttu-id="73e48-133">Семейств</span><span class="sxs-lookup"><span data-stu-id="73e48-133">Site</span></span>
<span data-ttu-id="73e48-134">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="73e48-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="73e48-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73e48-135">OUTPUTS</span></span>

## <span data-ttu-id="73e48-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="73e48-136">NOTES</span></span>

## <span data-ttu-id="73e48-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73e48-137">RELATED LINKS</span></span>

