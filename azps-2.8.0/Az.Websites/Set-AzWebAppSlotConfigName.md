---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: 5e2b13cd4c2586b15cc526aad3d922441b40265c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907845"
---
# <span data-ttu-id="86c37-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="86c37-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="86c37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86c37-102">SYNOPSIS</span></span>
<span data-ttu-id="86c37-103">Настройка имен конфигураций слотов веб-приложения</span><span class="sxs-lookup"><span data-stu-id="86c37-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="86c37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86c37-104">SYNTAX</span></span>

### <span data-ttu-id="86c37-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="86c37-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86c37-106">S2</span><span class="sxs-lookup"><span data-stu-id="86c37-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86c37-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c37-107">DESCRIPTION</span></span>
<span data-ttu-id="86c37-108">Командлет **Set-AzWebAppSlotConfigName** отмечает параметры приложения и строки соединения в качестве параметров слота.</span><span class="sxs-lookup"><span data-stu-id="86c37-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="86c37-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86c37-109">EXAMPLES</span></span>

### <span data-ttu-id="86c37-110">1:</span><span class="sxs-lookup"><span data-stu-id="86c37-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="86c37-111">Эта команда удаляет все параметры приложения и строки подключения для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="86c37-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="86c37-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86c37-112">PARAMETERS</span></span>

### <span data-ttu-id="86c37-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="86c37-113">-AppSettingNames</span></span>
<span data-ttu-id="86c37-114">Массив строк с именами параметров приложения</span><span class="sxs-lookup"><span data-stu-id="86c37-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="86c37-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="86c37-115">-ConnectionStringNames</span></span>
<span data-ttu-id="86c37-116">Массив строк соединения с именами строк</span><span class="sxs-lookup"><span data-stu-id="86c37-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="86c37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c37-117">-DefaultProfile</span></span>
<span data-ttu-id="86c37-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86c37-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86c37-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="86c37-119">-Name</span></span>
<span data-ttu-id="86c37-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="86c37-120">WebApp Name</span></span>

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

### <span data-ttu-id="86c37-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="86c37-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="86c37-122">Параметр "удалить все имена параметров приложений"</span><span class="sxs-lookup"><span data-stu-id="86c37-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="86c37-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="86c37-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="86c37-124">Параметр "удалить все имена строк подключения"</span><span class="sxs-lookup"><span data-stu-id="86c37-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="86c37-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c37-125">-ResourceGroupName</span></span>
<span data-ttu-id="86c37-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="86c37-126">Resource Group Name</span></span>

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

### <span data-ttu-id="86c37-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="86c37-127">-WebApp</span></span>
<span data-ttu-id="86c37-128">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="86c37-128">WebApp Object</span></span>

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

### <span data-ttu-id="86c37-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c37-129">CommonParameters</span></span>
<span data-ttu-id="86c37-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86c37-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c37-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c37-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c37-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86c37-132">INPUTS</span></span>

### <span data-ttu-id="86c37-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="86c37-133">System.String[]</span></span>

### <span data-ttu-id="86c37-134">System. String</span><span class="sxs-lookup"><span data-stu-id="86c37-134">System.String</span></span>

### <span data-ttu-id="86c37-135">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="86c37-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="86c37-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c37-136">OUTPUTS</span></span>

### <span data-ttu-id="86c37-137">Microsoft. Azure. Management. website. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="86c37-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="86c37-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="86c37-138">NOTES</span></span>

## <span data-ttu-id="86c37-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86c37-139">RELATED LINKS</span></span>
