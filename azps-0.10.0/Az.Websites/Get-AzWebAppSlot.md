---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910607"
---
# <span data-ttu-id="43434-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43434-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="43434-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43434-102">SYNOPSIS</span></span>
<span data-ttu-id="43434-103">Получает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="43434-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="43434-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43434-104">SYNTAX</span></span>

### <span data-ttu-id="43434-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="43434-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43434-106">S2</span><span class="sxs-lookup"><span data-stu-id="43434-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43434-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43434-107">DESCRIPTION</span></span>
<span data-ttu-id="43434-108">Командлет **Get-AzWebAppSlot** получает сведения о слоте веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="43434-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="43434-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43434-109">EXAMPLES</span></span>

### <span data-ttu-id="43434-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43434-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="43434-111">Эта команда получает слот с именем Slot001 из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="43434-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="43434-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43434-112">PARAMETERS</span></span>

### <span data-ttu-id="43434-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43434-113">-DefaultProfile</span></span>
<span data-ttu-id="43434-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43434-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43434-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43434-115">-Name</span></span>
<span data-ttu-id="43434-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="43434-116">WebApp Name</span></span>

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

### <span data-ttu-id="43434-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43434-117">-ResourceGroupName</span></span>
<span data-ttu-id="43434-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="43434-118">Resource Group Name</span></span>

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

### <span data-ttu-id="43434-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="43434-119">-Slot</span></span>
<span data-ttu-id="43434-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="43434-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="43434-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="43434-121">-WebApp</span></span>
<span data-ttu-id="43434-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="43434-122">WebApp Object</span></span>

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

### <span data-ttu-id="43434-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43434-123">CommonParameters</span></span>
<span data-ttu-id="43434-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43434-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43434-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43434-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43434-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43434-126">INPUTS</span></span>

### <span data-ttu-id="43434-127">Семейств</span><span class="sxs-lookup"><span data-stu-id="43434-127">Site</span></span>
<span data-ttu-id="43434-128">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="43434-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="43434-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43434-129">OUTPUTS</span></span>

## <span data-ttu-id="43434-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="43434-130">NOTES</span></span>

## <span data-ttu-id="43434-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43434-131">RELATED LINKS</span></span>

[<span data-ttu-id="43434-132">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43434-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="43434-133">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43434-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="43434-134">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43434-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="43434-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43434-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="43434-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43434-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="43434-137">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="43434-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="43434-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="43434-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
