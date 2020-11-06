---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 75c134b162636f94b00cf6692f4e9df120930dcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565272"
---
# <span data-ttu-id="5904e-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="5904e-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="5904e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5904e-102">SYNOPSIS</span></span>
<span data-ttu-id="5904e-103">Настройка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="5904e-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5904e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5904e-104">SYNTAX</span></span>

### <span data-ttu-id="5904e-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="5904e-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5904e-106">S2</span><span class="sxs-lookup"><span data-stu-id="5904e-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5904e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5904e-107">DESCRIPTION</span></span>
<span data-ttu-id="5904e-108">Командлет **Set-AzureRmWebAppSlotConfigName** отмечает параметры приложения и строки соединения в качестве параметров слота.</span><span class="sxs-lookup"><span data-stu-id="5904e-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="5904e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5904e-109">EXAMPLES</span></span>

### <span data-ttu-id="5904e-110">1:</span><span class="sxs-lookup"><span data-stu-id="5904e-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="5904e-111">Эта команда удаляет все параметры приложения и строки подключения для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="5904e-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5904e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5904e-112">PARAMETERS</span></span>

### <span data-ttu-id="5904e-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="5904e-113">-AppSettingNames</span></span>
<span data-ttu-id="5904e-114">Массив строк с именами параметров приложения</span><span class="sxs-lookup"><span data-stu-id="5904e-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="5904e-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="5904e-115">-ConnectionStringNames</span></span>
<span data-ttu-id="5904e-116">Массив строк соединения с именами строк</span><span class="sxs-lookup"><span data-stu-id="5904e-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="5904e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5904e-117">-DefaultProfile</span></span>
<span data-ttu-id="5904e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5904e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5904e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5904e-119">-Name</span></span>
<span data-ttu-id="5904e-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="5904e-120">WebApp Name</span></span>

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

### <span data-ttu-id="5904e-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="5904e-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="5904e-122">Параметр "удалить все имена параметров приложений"</span><span class="sxs-lookup"><span data-stu-id="5904e-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="5904e-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="5904e-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="5904e-124">Параметр "удалить все имена строк подключения"</span><span class="sxs-lookup"><span data-stu-id="5904e-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="5904e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5904e-125">-ResourceGroupName</span></span>
<span data-ttu-id="5904e-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5904e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="5904e-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5904e-127">-WebApp</span></span>
<span data-ttu-id="5904e-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="5904e-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5904e-129">CommonParameters</span></span>
<span data-ttu-id="5904e-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5904e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5904e-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5904e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5904e-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5904e-132">INPUTS</span></span>

### <span data-ttu-id="5904e-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="5904e-133">System.String[]</span></span>

### <span data-ttu-id="5904e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5904e-134">System.String</span></span>

### <span data-ttu-id="5904e-135">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="5904e-135">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="5904e-136">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5904e-136">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="5904e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5904e-137">OUTPUTS</span></span>

### <span data-ttu-id="5904e-138">Microsoft. Azure. Management. website. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="5904e-138">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="5904e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5904e-139">NOTES</span></span>

## <span data-ttu-id="5904e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5904e-140">RELATED LINKS</span></span>
