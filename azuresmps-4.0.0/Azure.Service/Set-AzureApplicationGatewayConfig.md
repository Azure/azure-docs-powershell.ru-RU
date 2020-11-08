---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076429"
---
# <span data-ttu-id="297aa-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="297aa-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="297aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="297aa-102">SYNOPSIS</span></span>
<span data-ttu-id="297aa-103">Настройка шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="297aa-103">Configures an application gateway.</span></span>

## <span data-ttu-id="297aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="297aa-104">SYNTAX</span></span>

### <span data-ttu-id="297aa-105">configFile</span><span class="sxs-lookup"><span data-stu-id="297aa-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="297aa-106">configObject</span><span class="sxs-lookup"><span data-stu-id="297aa-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="297aa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="297aa-107">DESCRIPTION</span></span>
<span data-ttu-id="297aa-108">Командлет **Set-AzureApplicationGatewayConfig** настраивает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="297aa-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="297aa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="297aa-109">EXAMPLES</span></span>

### <span data-ttu-id="297aa-110">Пример 1: Настройка шлюза приложений с помощью объекта конфигурации</span><span class="sxs-lookup"><span data-stu-id="297aa-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="297aa-111">Первая команда получает объект конфигурации для шлюза приложения с именем ApplicationGateway02 с помощью командлета **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="297aa-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="297aa-112">Команда сохраняет его в переменной $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="297aa-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="297aa-113">Вторая команда задает конфигурацию для приложения с именем ApplicationGateway06, используя объект конфигурации шлюза приложения, хранящийся в переменной $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="297aa-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="297aa-114">Пример 2: Настройка шлюза приложений с помощью файла конфигурации</span><span class="sxs-lookup"><span data-stu-id="297aa-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="297aa-115">Эта команда задает конфигурацию для приложения с именем ApplicationGateway06 с помощью файла конфигурации шлюза приложений в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="297aa-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="297aa-116">Пример 3: изменение конфигурации с помощью объекта конфигурации</span><span class="sxs-lookup"><span data-stu-id="297aa-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="297aa-117">Первая команда получает объект конфигурации для шлюза приложения с именем ApplicationGateway06 с помощью командлета **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="297aa-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="297aa-118">Команда сохраняет его в переменной $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="297aa-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="297aa-119">Вторая команда назначает значение порта свойству **Port** в объекте, хранящемся в $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="297aa-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="297aa-120">Последняя команда передает обновленный $ConfigReturnObject текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="297aa-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="297aa-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="297aa-121">PARAMETERS</span></span>

### <span data-ttu-id="297aa-122">-Config</span><span class="sxs-lookup"><span data-stu-id="297aa-122">-Config</span></span>
<span data-ttu-id="297aa-123">Указывает объект конфигурации шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="297aa-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="297aa-124">Этот командлет назначает конфигурацию, которую этот параметр указывает на шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="297aa-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="297aa-125">-ConfigFile</span><span class="sxs-lookup"><span data-stu-id="297aa-125">-ConfigFile</span></span>
<span data-ttu-id="297aa-126">Задает путь к файлу конфигурации в формате XML для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="297aa-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="297aa-127">Этот командлет назначает конфигурацию, которую этот параметр указывает на шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="297aa-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="297aa-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="297aa-128">-Name</span></span>
<span data-ttu-id="297aa-129">Указывает имя шлюза приложений, который настраивает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="297aa-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="297aa-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="297aa-130">-Profile</span></span>
<span data-ttu-id="297aa-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="297aa-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="297aa-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="297aa-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="297aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297aa-133">CommonParameters</span></span>
<span data-ttu-id="297aa-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="297aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297aa-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="297aa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297aa-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="297aa-136">INPUTS</span></span>

### <span data-ttu-id="297aa-137">System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="297aa-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="297aa-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="297aa-138">OUTPUTS</span></span>

### <span data-ttu-id="297aa-139">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="297aa-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="297aa-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="297aa-140">NOTES</span></span>

## <span data-ttu-id="297aa-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="297aa-141">RELATED LINKS</span></span>

[<span data-ttu-id="297aa-142">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="297aa-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


