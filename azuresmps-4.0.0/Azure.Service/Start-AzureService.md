---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076030"
---
# <span data-ttu-id="71a5e-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="71a5e-101">Start-AzureService</span></span>

## <span data-ttu-id="71a5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="71a5e-103">Запускает указанную размещенную службу в Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="71a5e-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="71a5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71a5e-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="71a5e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71a5e-105">DESCRIPTION</span></span>
<span data-ttu-id="71a5e-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="71a5e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="71a5e-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="71a5e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="71a5e-108">Командлет **Start-AzureService** запускает указанную размещенную службу в Windows Azure, если она находится в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="71a5e-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="71a5e-109">Обратите внимание, что командлет **Publish-AzureServiceProject** автоматически пытается запустить службу.</span><span class="sxs-lookup"><span data-stu-id="71a5e-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="71a5e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71a5e-110">EXAMPLES</span></span>

## <span data-ttu-id="71a5e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71a5e-111">PARAMETERS</span></span>

### <span data-ttu-id="71a5e-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71a5e-112">-PassThru</span></span>
<span data-ttu-id="71a5e-113">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="71a5e-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="71a5e-114">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="71a5e-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71a5e-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="71a5e-115">-Profile</span></span>
<span data-ttu-id="71a5e-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="71a5e-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71a5e-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71a5e-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a5e-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="71a5e-118">-ServiceName</span></span>
<span data-ttu-id="71a5e-119">Указывает имя размещенной службы для запуска.</span><span class="sxs-lookup"><span data-stu-id="71a5e-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="71a5e-120">Если имя не указано, командлет запускает текущую размещенную службу.</span><span class="sxs-lookup"><span data-stu-id="71a5e-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a5e-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="71a5e-121">-Slot</span></span>
<span data-ttu-id="71a5e-122">Указывает слот развертывания, в котором запускается служба: промежуточный или производственный.</span><span class="sxs-lookup"><span data-stu-id="71a5e-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a5e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a5e-123">CommonParameters</span></span>
<span data-ttu-id="71a5e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71a5e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a5e-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a5e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a5e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71a5e-126">INPUTS</span></span>

## <span data-ttu-id="71a5e-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71a5e-127">OUTPUTS</span></span>

## <span data-ttu-id="71a5e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="71a5e-128">NOTES</span></span>

## <span data-ttu-id="71a5e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71a5e-129">RELATED LINKS</span></span>

[<span data-ttu-id="71a5e-130">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="71a5e-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="71a5e-131">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="71a5e-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="71a5e-132">Остановить-AzureService</span><span class="sxs-lookup"><span data-stu-id="71a5e-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


