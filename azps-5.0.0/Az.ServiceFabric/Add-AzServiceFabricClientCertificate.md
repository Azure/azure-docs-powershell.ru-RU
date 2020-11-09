---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246829"
---
# <span data-ttu-id="12fdf-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="12fdf-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="12fdf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="12fdf-103">Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="12fdf-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="12fdf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12fdf-104">SYNTAX</span></span>

### <span data-ttu-id="12fdf-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="12fdf-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fdf-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="12fdf-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fdf-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="12fdf-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12fdf-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="12fdf-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12fdf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12fdf-109">DESCRIPTION</span></span>
<span data-ttu-id="12fdf-110">С помощью **Add-AzServiceFabricClientCertificate** добавьте в кластер общего имени и отпечаток поставщика или отпечаток сертификата, чтобы клиент мог использовать его для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="12fdf-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="12fdf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12fdf-111">EXAMPLES</span></span>

### <span data-ttu-id="12fdf-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12fdf-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="12fdf-113">Эта команда добавит сертификат с отпечатком "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер, чтобы клиент мог использовать этот сертификат в качестве администратора для связи с кластером.</span><span class="sxs-lookup"><span data-stu-id="12fdf-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="12fdf-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="12fdf-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="12fdf-115">Эта команда добавит сертификат клиента только для чтения с общим именем "Contoso.com", а отпечаток поставщика — "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер.</span><span class="sxs-lookup"><span data-stu-id="12fdf-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="12fdf-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12fdf-116">PARAMETERS</span></span>

### <span data-ttu-id="12fdf-117">-Администратор</span><span class="sxs-lookup"><span data-stu-id="12fdf-117">-Admin</span></span>
<span data-ttu-id="12fdf-118">Тип проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="12fdf-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="12fdf-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="12fdf-120">Укажите отпечаток сертификата клиента с разрешением администратора.</span><span class="sxs-lookup"><span data-stu-id="12fdf-120">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="12fdf-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="12fdf-122">Укажите общее имя клиента, отпечаток поставщика и тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="12fdf-122">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="12fdf-123">-CommonName</span></span>
<span data-ttu-id="12fdf-124">Указание общего имени сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="12fdf-124">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fdf-125">-DefaultProfile</span></span>
<span data-ttu-id="12fdf-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12fdf-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12fdf-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="12fdf-127">-IssuerThumbprint</span></span>
<span data-ttu-id="12fdf-128">Указание отпечатка поставщика сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="12fdf-128">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12fdf-129">-Name</span></span>
<span data-ttu-id="12fdf-130">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="12fdf-130">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="12fdf-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="12fdf-132">Укажите отпечаток сертификата клиента с разрешением только на чтение</span><span class="sxs-lookup"><span data-stu-id="12fdf-132">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fdf-133">-ResourceGroupName</span></span>
<span data-ttu-id="12fdf-134">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12fdf-134">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-135">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="12fdf-135">-Thumbprint</span></span>
<span data-ttu-id="12fdf-136">Указание отпечатка сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="12fdf-136">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12fdf-137">-Confirm</span></span>
<span data-ttu-id="12fdf-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12fdf-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12fdf-139">-WhatIf</span></span>
<span data-ttu-id="12fdf-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12fdf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12fdf-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12fdf-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12fdf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fdf-142">CommonParameters</span></span>
<span data-ttu-id="12fdf-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12fdf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fdf-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12fdf-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fdf-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12fdf-145">INPUTS</span></span>

### <span data-ttu-id="12fdf-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="12fdf-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="12fdf-147">System. String</span><span class="sxs-lookup"><span data-stu-id="12fdf-147">System.String</span></span>

### <span data-ttu-id="12fdf-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="12fdf-148">System.String[]</span></span>

### <span data-ttu-id="12fdf-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="12fdf-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="12fdf-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12fdf-150">OUTPUTS</span></span>

### <span data-ttu-id="12fdf-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="12fdf-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="12fdf-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="12fdf-152">NOTES</span></span>

## <span data-ttu-id="12fdf-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12fdf-153">RELATED LINKS</span></span>

[<span data-ttu-id="12fdf-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="12fdf-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)