---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505746"
---
# <span data-ttu-id="955e2-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="955e2-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="955e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="955e2-102">SYNOPSIS</span></span>
<span data-ttu-id="955e2-103">Удаляет привязку SSL из загруженного сертификата.</span><span class="sxs-lookup"><span data-stu-id="955e2-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="955e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="955e2-104">SYNTAX</span></span>

### <span data-ttu-id="955e2-105">S1</span><span class="sxs-lookup"><span data-stu-id="955e2-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="955e2-106">S2</span><span class="sxs-lookup"><span data-stu-id="955e2-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="955e2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="955e2-107">DESCRIPTION</span></span>
<span data-ttu-id="955e2-108">С **помощью cmdlet Remove-AzWebAppSSLBinding** удаляется привязка SSL из Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="955e2-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="955e2-109">Привязки SSL используются для связывания Веб-приложения с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="955e2-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="955e2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="955e2-110">EXAMPLES</span></span>

### <span data-ttu-id="955e2-111">Пример 1. Удаление привязки SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="955e2-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="955e2-112">Эта команда удаляет привязку SSL для веб-приложения ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="955e2-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="955e2-113">Так как *параметр DeleteCertificate* не включен, сертификат будет удален, если он больше не имеет привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="955e2-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="955e2-114">Пример 2. Удаление привязки SSL без удаления сертификата</span><span class="sxs-lookup"><span data-stu-id="955e2-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="955e2-115">Как и в примере 1, эта команда также удаляет привязку SSL для веб-приложения ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="955e2-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="955e2-116">Однако в этом случае параметр *DeleteCertificate* включается, а его значением является $False.</span><span class="sxs-lookup"><span data-stu-id="955e2-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="955e2-117">Это означает, что сертификат не будет удален независимо от того, имеет ли он привязку SSL.</span><span class="sxs-lookup"><span data-stu-id="955e2-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="955e2-118">Пример 3. Удаление привязки SSL с помощью ссылки на объект</span><span class="sxs-lookup"><span data-stu-id="955e2-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="955e2-119">В этом примере используется ссылка на веб-сайт Web App для удаления привязки SSL для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="955e2-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="955e2-120">Первая команда использует Get-AzWebApp для создания ссылки на объект с именем ContosoWebApp в приложении Web App.</span><span class="sxs-lookup"><span data-stu-id="955e2-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="955e2-121">Эта ссылка на объект хранится в переменной с именем $WebApp.</span><span class="sxs-lookup"><span data-stu-id="955e2-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="955e2-122">Вторая команда использует ссылку на объект и командлет **Remove-AzWebAppSSLBinding** для удаления привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="955e2-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="955e2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="955e2-123">PARAMETERS</span></span>

### <span data-ttu-id="955e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955e2-124">-DefaultProfile</span></span>
<span data-ttu-id="955e2-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="955e2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="955e2-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="955e2-126">-DeleteCertificate</span></span>
<span data-ttu-id="955e2-127">Указывает действие, которое будет происходить, если SSL-привязка удаляется только из сертификата.</span><span class="sxs-lookup"><span data-stu-id="955e2-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="955e2-128">Если *для действия DeleteCertificate* задано значение $False, сертификат не будет удален при удалении привязки.</span><span class="sxs-lookup"><span data-stu-id="955e2-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="955e2-129">Если *команда DeleteCertificate* имеет значение $True или не включена в команду, сертификат будет удален вместе с привязкой SSL.</span><span class="sxs-lookup"><span data-stu-id="955e2-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="955e2-130">Сертификат удаляется только в том случае, если удаляется привязка SSL.</span><span class="sxs-lookup"><span data-stu-id="955e2-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="955e2-131">Если сертификат имеет несколько привязки, сертификат не будет удален независимо от значения параметра *DeleteCertificate.*</span><span class="sxs-lookup"><span data-stu-id="955e2-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

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

### <span data-ttu-id="955e2-132">-Force</span><span class="sxs-lookup"><span data-stu-id="955e2-132">-Force</span></span>
<span data-ttu-id="955e2-133">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="955e2-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="955e2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="955e2-134">-Name</span></span>
<span data-ttu-id="955e2-135">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="955e2-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="955e2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="955e2-136">-ResourceGroupName</span></span>
<span data-ttu-id="955e2-137">Имя группы ресурсов, которая назначена сертификату.</span><span class="sxs-lookup"><span data-stu-id="955e2-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="955e2-138">В одной команде нельзя использовать параметр *ResourceGroupName* и *параметр WebApp.*</span><span class="sxs-lookup"><span data-stu-id="955e2-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="955e2-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="955e2-139">-Slot</span></span>
<span data-ttu-id="955e2-140">Указывает слот развертывания Web App.</span><span class="sxs-lookup"><span data-stu-id="955e2-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="955e2-141">Чтобы получить слот развертывания, воспользуйтесь Get-AzWebAppSlot управления.</span><span class="sxs-lookup"><span data-stu-id="955e2-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="955e2-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="955e2-142">-WebApp</span></span>
<span data-ttu-id="955e2-143">Определяет веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="955e2-143">Specifies a Web App.</span></span>
<span data-ttu-id="955e2-144">Чтобы получить веб-приложение, воспользуйтесь Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="955e2-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="955e2-145">Нельзя использовать параметр *WebApp* в той же команде, что и параметр *ResourceGroupName* или *WebAppName.*</span><span class="sxs-lookup"><span data-stu-id="955e2-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="955e2-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="955e2-146">-WebAppName</span></span>
<span data-ttu-id="955e2-147">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="955e2-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="955e2-148">В одной команде нельзя использовать *параметры WebAppName* и *WebApp.*</span><span class="sxs-lookup"><span data-stu-id="955e2-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="955e2-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="955e2-149">-Confirm</span></span>
<span data-ttu-id="955e2-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="955e2-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="955e2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="955e2-151">-WhatIf</span></span>
<span data-ttu-id="955e2-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="955e2-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="955e2-153">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="955e2-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="955e2-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="955e2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="955e2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955e2-155">CommonParameters</span></span>
<span data-ttu-id="955e2-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955e2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955e2-157">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="955e2-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955e2-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="955e2-158">INPUTS</span></span>

### <span data-ttu-id="955e2-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="955e2-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="955e2-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="955e2-160">OUTPUTS</span></span>

### <span data-ttu-id="955e2-161">System.Void</span><span class="sxs-lookup"><span data-stu-id="955e2-161">System.Void</span></span>

## <span data-ttu-id="955e2-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="955e2-162">NOTES</span></span>

## <span data-ttu-id="955e2-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="955e2-163">RELATED LINKS</span></span>

[<span data-ttu-id="955e2-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="955e2-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="955e2-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="955e2-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="955e2-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="955e2-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="955e2-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="955e2-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


