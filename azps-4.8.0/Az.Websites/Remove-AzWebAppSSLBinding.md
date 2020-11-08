---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079301"
---
# <span data-ttu-id="f6e8e-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6e8e-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="f6e8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e8e-103">Удаление привязки SSL из отправленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="f6e8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6e8e-104">SYNTAX</span></span>

### <span data-ttu-id="f6e8e-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="f6e8e-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6e8e-106">S2</span><span class="sxs-lookup"><span data-stu-id="f6e8e-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6e8e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6e8e-107">DESCRIPTION</span></span>
<span data-ttu-id="f6e8e-108">Командлет **Remove-AzWebAppSSLBinding** удаляет привязку SSL (Secure Sockets Layer) из веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="f6e8e-109">Привязки SSL используются для связывания веб-приложения с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="f6e8e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6e8e-110">EXAMPLES</span></span>

### <span data-ttu-id="f6e8e-111">Пример 1: удаление привязки SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="f6e8e-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="f6e8e-112">Эта команда удаляет привязку SSL для веб-приложения ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="f6e8e-113">Так как параметр *DeleteCertificate* не включен, сертификат будет удален, если он больше не имеет каких-либо SSL-привязок.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="f6e8e-114">Пример 2: удаление привязки SSL без удаления сертификата</span><span class="sxs-lookup"><span data-stu-id="f6e8e-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="f6e8e-115">Как и в примере 1, эта команда также удаляет привязку SSL для веб-приложения ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="f6e8e-116">Тем не менее, в этом случае параметр *DeleteCertificate* включается, и значение параметра задается равным $false.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="f6e8e-117">Это означает, что сертификат не будет удален независимо от того, есть ли у него привязки SSL или нет.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="f6e8e-118">Пример 3: использование ссылки на объект для удаления привязки SSL</span><span class="sxs-lookup"><span data-stu-id="f6e8e-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="f6e8e-119">В этом примере для удаления привязки SSL для веб-приложения используется ссылка на объект веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="f6e8e-120">Первая команда использует командлет Get-AzWebApp для создания ссылки на объект веб-приложения с именем ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="f6e8e-121">Ссылка на объект хранится в переменной с именем $WebApp.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="f6e8e-122">Вторая команда использует ссылку на объект и командлет **Remove-AzWebAppSSLBinding** для удаления привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="f6e8e-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6e8e-123">PARAMETERS</span></span>

### <span data-ttu-id="f6e8e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e8e-124">-DefaultProfile</span></span>
<span data-ttu-id="f6e8e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6e8e-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="f6e8e-126">-DeleteCertificate</span></span>
<span data-ttu-id="f6e8e-127">Указывает действие, которое будет выполнено, если удаляемая привязка SSL является единственной привязкой, используемой сертификатом.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="f6e8e-128">Если для *DeleteCertificate* задано значение $false, сертификат не будет удален при удалении привязки.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="f6e8e-129">Если *DeleteCertificate* имеет значение $true или не включено в команду, сертификат будет удален вместе с привязкой SSL.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="f6e8e-130">Сертификат будет удален только в том случае, если удаляемая привязка SSL является единственной привязкой, используемой сертификатом.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="f6e8e-131">Если у сертификата есть более одной привязки, сертификат не будет удален независимо от значения параметра *DeleteCertificate* .</span><span class="sxs-lookup"><span data-stu-id="f6e8e-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e8e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f6e8e-132">-Force</span></span>
<span data-ttu-id="f6e8e-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6e8e-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6e8e-134">-Name</span></span>
<span data-ttu-id="f6e8e-135">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e8e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e8e-136">-ResourceGroupName</span></span>
<span data-ttu-id="f6e8e-137">Указывает имя группы ресурсов, которой назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="f6e8e-138">В одной команде нельзя использовать параметры *ResourceGroupName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="f6e8e-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="f6e8e-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="f6e8e-139">-Slot</span></span>
<span data-ttu-id="f6e8e-140">Указывает слот развертывания веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="f6e8e-141">Чтобы получить слот развертывания, используйте командлет Get-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="f6e8e-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f6e8e-142">-WebApp</span></span>
<span data-ttu-id="f6e8e-143">Указывает веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-143">Specifies a Web App.</span></span>
<span data-ttu-id="f6e8e-144">Чтобы получить веб-приложение, используйте командлет Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="f6e8e-145">Параметр *webapp* нельзя использовать в той же команде, что и параметр *ResourceGroupName* , и (или) *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="f6e8e-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f6e8e-146">-WebAppName</span></span>
<span data-ttu-id="f6e8e-147">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="f6e8e-148">В одной команде нельзя использовать параметры *WebAppName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="f6e8e-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="f6e8e-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6e8e-149">-Confirm</span></span>
<span data-ttu-id="f6e8e-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e8e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6e8e-151">-WhatIf</span></span>
<span data-ttu-id="f6e8e-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6e8e-153">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6e8e-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e8e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e8e-155">CommonParameters</span></span>
<span data-ttu-id="f6e8e-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6e8e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e8e-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6e8e-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e8e-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6e8e-158">INPUTS</span></span>

### <span data-ttu-id="f6e8e-159">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="f6e8e-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f6e8e-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6e8e-160">OUTPUTS</span></span>

### <span data-ttu-id="f6e8e-161">System. void</span><span class="sxs-lookup"><span data-stu-id="f6e8e-161">System.Void</span></span>

## <span data-ttu-id="f6e8e-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6e8e-162">NOTES</span></span>

## <span data-ttu-id="f6e8e-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6e8e-163">RELATED LINKS</span></span>

[<span data-ttu-id="f6e8e-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6e8e-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="f6e8e-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f6e8e-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="f6e8e-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6e8e-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f6e8e-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f6e8e-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

