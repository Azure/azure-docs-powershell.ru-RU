---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 975b49af1e20c5b9f4839a561494eaeb8275f02f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910571"
---
# <span data-ttu-id="8511d-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="8511d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8511d-102">SYNOPSIS</span></span>
<span data-ttu-id="8511d-103">Перезапускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="8511d-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="8511d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8511d-104">SYNTAX</span></span>

### <span data-ttu-id="8511d-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="8511d-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8511d-106">S2</span><span class="sxs-lookup"><span data-stu-id="8511d-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8511d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8511d-107">DESCRIPTION</span></span>
<span data-ttu-id="8511d-108">Командлет **restart-AzWebApp** останавливается, а затем запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="8511d-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="8511d-109">Если веб-приложение находится в остановленном состоянии, используйте командлет Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="8511d-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="8511d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8511d-110">EXAMPLES</span></span>

### <span data-ttu-id="8511d-111">Пример 1: перезагрузка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="8511d-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8511d-112">Эта команда останавливает веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов Default-Web-WestUS, а затем перезапускает ее.</span><span class="sxs-lookup"><span data-stu-id="8511d-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="8511d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8511d-113">PARAMETERS</span></span>

### <span data-ttu-id="8511d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8511d-114">-DefaultProfile</span></span>
<span data-ttu-id="8511d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8511d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8511d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8511d-116">-Name</span></span>
<span data-ttu-id="8511d-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-117">WebApp Name</span></span>

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

### <span data-ttu-id="8511d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8511d-118">-ResourceGroupName</span></span>
<span data-ttu-id="8511d-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8511d-119">Resource Group Name</span></span>

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

### <span data-ttu-id="8511d-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-120">-WebApp</span></span>
<span data-ttu-id="8511d-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-121">WebApp Object</span></span>

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

### <span data-ttu-id="8511d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8511d-122">CommonParameters</span></span>
<span data-ttu-id="8511d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8511d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8511d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8511d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8511d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8511d-125">INPUTS</span></span>

### <span data-ttu-id="8511d-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="8511d-126">Site</span></span>
<span data-ttu-id="8511d-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8511d-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8511d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8511d-128">OUTPUTS</span></span>

## <span data-ttu-id="8511d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8511d-129">NOTES</span></span>

## <span data-ttu-id="8511d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8511d-130">RELATED LINKS</span></span>

[<span data-ttu-id="8511d-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="8511d-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8511d-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8511d-134">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="8511d-135">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8511d-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


