---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235173"
---
# <span data-ttu-id="591e0-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="591e0-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="591e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="591e0-102">SYNOPSIS</span></span>
<span data-ttu-id="591e0-103">Получение привязки SSL сертификата веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="591e0-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="591e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="591e0-104">SYNTAX</span></span>

### <span data-ttu-id="591e0-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="591e0-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="591e0-106">S2</span><span class="sxs-lookup"><span data-stu-id="591e0-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="591e0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="591e0-107">DESCRIPTION</span></span>
<span data-ttu-id="591e0-108">Командлет **Get-AzWebAppSSLBinding** получает для веб-приложения Azure привязку SSL (Secure socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="591e0-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="591e0-109">Привязки SSL используются для связывания веб-приложения с отправленным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="591e0-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="591e0-110">Веб-приложения можно привязать к нескольким сертификатам.</span><span class="sxs-lookup"><span data-stu-id="591e0-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="591e0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="591e0-111">EXAMPLES</span></span>

### <span data-ttu-id="591e0-112">Пример 1: получение привязок SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="591e0-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="591e0-113">Эта команда извлекает привязки SSL для веб-приложения ContosoWebApp, связанного с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="591e0-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="591e0-114">Пример 2: использование ссылки на объект для получения привязок SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="591e0-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="591e0-115">Команды в этом примере также получают привязки SSL для веб-приложения ContosoWebApp; Однако в этом случае вместо имени веб-приложения и имени связанной группы ресурсов используется ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="591e0-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="591e0-116">Эта ссылка на объект создана первой командой в примере, которая использует **Get-AzWebApp** для создания ссылки на объект веб-приложения с именем ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="591e0-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="591e0-117">Ссылка на объект хранится в переменной с именем $WebApp.</span><span class="sxs-lookup"><span data-stu-id="591e0-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="591e0-118">Эта переменная и командлет **Get-AzWebAppSSLBinding** используются второй командой для получения привязок SSL.</span><span class="sxs-lookup"><span data-stu-id="591e0-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="591e0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="591e0-119">PARAMETERS</span></span>

### <span data-ttu-id="591e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591e0-120">-DefaultProfile</span></span>
<span data-ttu-id="591e0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="591e0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="591e0-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="591e0-122">-Name</span></span>
<span data-ttu-id="591e0-123">Указывает имя привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="591e0-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="591e0-125">Указывает имя группы ресурсов, которой назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="591e0-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="591e0-126">В одной команде нельзя использовать параметры *ResourceGroupName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="591e0-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="591e0-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="591e0-127">-Slot</span></span>
<span data-ttu-id="591e0-128">Указывает слот развертывания веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="591e0-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="591e0-129">Чтобы получить слот развертывания, используйте командлет Get-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="591e0-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591e0-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="591e0-130">-WebApp</span></span>
<span data-ttu-id="591e0-131">Указывает веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="591e0-131">Specifies a Web App.</span></span>
<span data-ttu-id="591e0-132">Чтобы получить веб-приложение, используйте командлет Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="591e0-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="591e0-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="591e0-133">-WebAppName</span></span>
<span data-ttu-id="591e0-134">Указывает имя веб-приложения, из которого этот командлет получает привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="591e0-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="591e0-135">В одной команде нельзя использовать параметры *WebAppName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="591e0-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591e0-136">CommonParameters</span></span>
<span data-ttu-id="591e0-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="591e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591e0-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591e0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591e0-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="591e0-139">INPUTS</span></span>

### <span data-ttu-id="591e0-140">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="591e0-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="591e0-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="591e0-141">OUTPUTS</span></span>

### <span data-ttu-id="591e0-142">Microsoft. Azure. Management. website. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="591e0-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="591e0-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="591e0-143">NOTES</span></span>

## <span data-ttu-id="591e0-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="591e0-144">RELATED LINKS</span></span>

[<span data-ttu-id="591e0-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="591e0-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="591e0-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="591e0-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="591e0-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="591e0-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


