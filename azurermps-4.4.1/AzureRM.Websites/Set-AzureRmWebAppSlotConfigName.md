---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557676"
---
# <span data-ttu-id="5abef-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="5abef-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="5abef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5abef-102">SYNOPSIS</span></span>
<span data-ttu-id="5abef-103">Настройка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="5abef-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5abef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5abef-104">SYNTAX</span></span>

### <span data-ttu-id="5abef-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="5abef-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5abef-106">S2</span><span class="sxs-lookup"><span data-stu-id="5abef-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5abef-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5abef-107">DESCRIPTION</span></span>
<span data-ttu-id="5abef-108">Командлет **Set-AzureRmWebAppSlotConfigName** отмечает параметры приложения и строки соединения в качестве параметров слота.</span><span class="sxs-lookup"><span data-stu-id="5abef-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="5abef-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5abef-109">EXAMPLES</span></span>

### <span data-ttu-id="5abef-110">1:</span><span class="sxs-lookup"><span data-stu-id="5abef-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="5abef-111">Эта команда удаляет все параметры приложения и строки подключения для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="5abef-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5abef-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5abef-112">PARAMETERS</span></span>

### <span data-ttu-id="5abef-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="5abef-113">-AppSettingNames</span></span>
<span data-ttu-id="5abef-114">Массив строк с именами параметров приложения</span><span class="sxs-lookup"><span data-stu-id="5abef-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5abef-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="5abef-115">-ConnectionStringNames</span></span>
<span data-ttu-id="5abef-116">Массив строк соединения с именами строк</span><span class="sxs-lookup"><span data-stu-id="5abef-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5abef-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5abef-117">-Name</span></span>
<span data-ttu-id="5abef-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="5abef-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5abef-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="5abef-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="5abef-120">Параметр "удалить все имена параметров приложений"</span><span class="sxs-lookup"><span data-stu-id="5abef-120">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abef-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="5abef-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="5abef-122">Параметр "удалить все имена строк подключения"</span><span class="sxs-lookup"><span data-stu-id="5abef-122">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5abef-123">-ResourceGroupName</span></span>
<span data-ttu-id="5abef-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5abef-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abef-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5abef-125">-WebApp</span></span>
<span data-ttu-id="5abef-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="5abef-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5abef-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5abef-127">-DefaultProfile</span></span>
<span data-ttu-id="5abef-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5abef-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5abef-129">CommonParameters</span></span>
<span data-ttu-id="5abef-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5abef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5abef-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5abef-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5abef-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5abef-132">INPUTS</span></span>

### <span data-ttu-id="5abef-133">Семейств</span><span class="sxs-lookup"><span data-stu-id="5abef-133">Site</span></span>
<span data-ttu-id="5abef-134">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5abef-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5abef-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5abef-135">OUTPUTS</span></span>

## <span data-ttu-id="5abef-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="5abef-136">NOTES</span></span>

## <span data-ttu-id="5abef-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5abef-137">RELATED LINKS</span></span>

