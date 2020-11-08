---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076355"
---
# <span data-ttu-id="6d3f8-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6d3f8-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="6d3f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3f8-103">Получает сведения о развертывании.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="6d3f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d3f8-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6d3f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d3f8-105">DESCRIPTION</span></span>
<span data-ttu-id="6d3f8-106">Командлет **Get-AzureDeployment** получает сведения о развертывании Azure.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="6d3f8-107">Укажите имя службы Azure и ячейку развертывания.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="6d3f8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d3f8-108">EXAMPLES</span></span>

### <span data-ttu-id="6d3f8-109">Пример 1: получение сведений о рабочем развертывании</span><span class="sxs-lookup"><span data-stu-id="6d3f8-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="6d3f8-110">Эта команда возвращает сведения о развертывании для службы с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="6d3f8-111">В этой команде не указана ячейка.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-111">This command does not specify a slot.</span></span>
<span data-ttu-id="6d3f8-112">Поэтому в команде используется значение по умолчанию "производство".</span><span class="sxs-lookup"><span data-stu-id="6d3f8-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="6d3f8-113">Пример 2: получение подробных сведений о промежуточном развертывании</span><span class="sxs-lookup"><span data-stu-id="6d3f8-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="6d3f8-114">Эта команда возвращает сведения о промежуточном развертывании ContosoService.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="6d3f8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d3f8-115">PARAMETERS</span></span>

### <span data-ttu-id="6d3f8-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6d3f8-116">-InformationAction</span></span>
<span data-ttu-id="6d3f8-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6d3f8-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6d3f8-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d3f8-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6d3f8-119">Continue</span></span>
- <span data-ttu-id="6d3f8-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6d3f8-120">Ignore</span></span>
- <span data-ttu-id="6d3f8-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6d3f8-121">Inquire</span></span>
- <span data-ttu-id="6d3f8-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6d3f8-122">SilentlyContinue</span></span>
- <span data-ttu-id="6d3f8-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="6d3f8-123">Stop</span></span>
- <span data-ttu-id="6d3f8-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="6d3f8-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3f8-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6d3f8-125">-InformationVariable</span></span>
<span data-ttu-id="6d3f8-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3f8-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="6d3f8-127">-Profile</span></span>
<span data-ttu-id="6d3f8-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6d3f8-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6d3f8-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6d3f8-130">-ServiceName</span></span>
<span data-ttu-id="6d3f8-131">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-131">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3f8-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="6d3f8-132">-Slot</span></span>
<span data-ttu-id="6d3f8-133">Задает среду развертывания.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="6d3f8-134">Допустимые значения: промежуточный или производственный.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="6d3f8-135">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="6d3f8-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3f8-136">CommonParameters</span></span>
<span data-ttu-id="6d3f8-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d3f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3f8-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d3f8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3f8-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d3f8-139">INPUTS</span></span>

## <span data-ttu-id="6d3f8-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d3f8-140">OUTPUTS</span></span>

## <span data-ttu-id="6d3f8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d3f8-141">NOTES</span></span>

## <span data-ttu-id="6d3f8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d3f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d3f8-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="6d3f8-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="6d3f8-144">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6d3f8-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="6d3f8-145">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6d3f8-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="6d3f8-146">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6d3f8-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="6d3f8-147">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="6d3f8-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


